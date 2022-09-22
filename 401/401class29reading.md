[<=== Back](../README.md)

# Rooms
*from developer.android.com*


## [Save data in a local database using Room](https://developer.android.com/training/data-storage/room)


> Apps that handle non-trivial amounts of structured data can benefit greatly from persisting that data locally. The most common use case is to cache relevant pieces of data so that when the device cannot access the network, the user can still browse that content while they are offline.

**Three primary components in Room**

- The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.

- Data entities that represent tables in your app's database.

- Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

![Room components](img/room_architecture.png)


## [Defining data using Room entities](https://developer.android.com/training/data-storage/room/defining-data)

> When you use the Room persistence library to store your app's data, you define entities to represent the objects that you want to store. Each entity corresponds to a table in the associated Room database, and each instance of an entity represents a row of data in the corresponding table.

That means you can use Room entities to define your database schema without writing any SQL code.

Example code:

```
@Entity
public class User {
    @PrimaryKey
    public int id;

    public String firstName;
    public String lastName;
}
```

Each Room must define a primary key: 

```@PrimaryKey
public int id;
```

## [Define relationships between objects](https://developer.android.com/training/data-storage/room/relationships)

> Because SQLite is a relational database, you can define relationships between entities. Even though most object-relational mapping libraries allow entity objects to reference each other, Room explicitly forbids this. To learn about the technical reasoning behind this decision, see Understand why Room doesn't allow object references.

There are two ways to define and query a relationship between entities: model the relationship with an intermediate data class, or use a relational query method with a multimap return type.


### Create Embedded Objects

> Sometimes, you'd like to express an entity or data object as a cohesive whole in your database logic, even if the object contains several fields. In these situations, you can use the @Embedded annotation to represent an object that you'd like to decompose into its subfields within a table. You can then query the embedded fields just as you would for other individual columns.

Example:

```
public class Address {
    public String street;
    public String state;
    public String city;

    @ColumnInfo(name = "post_code") public int postCode;
}

@Entity
public class User {
    @PrimaryKey public int id;

    public String firstName;

    @Embedded public Address address;
}
```

### One-to-one relationships

```
@Entity
public class User {
    @PrimaryKey public long userId;
    public String name;
    public int age;
}

@Entity
public class Library {
    @PrimaryKey public long libraryId;
    public long userOwnerId;
}
```

### One-to-many relationships

```
@Entity
public class User {
    @PrimaryKey public long userId;
    public String name;
    public int age;
}

@Entity
public class Playlist {
    @PrimaryKey public long playlistId;
    public long userCreatorId;
    public String playlistName;
}
```

## [Accessing data using Room DAOs](https://developer.android.com/training/data-storage/room/accessing-data#java)

> When you use the Room persistence library to store your app's data, you interact with the stored data by defining data access objects, or DAOs. Each DAO includes methods that offer abstract access to your app's database. At compile time, Room automatically generates implementations of the DAOs that you define.

> By using DAOs to access your app's database instead of query builders or direct queries, you can preserve separation of concerns, a critical architectural principle. DAOs also make it easier for you to mock database access when you test your app.

DAO's can be defined as either an interface or an abstract class. Interface is used in basic cases.

```
@Dao
public interface UserDao {
    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);

    @Query("SELECT * FROM user")
    List<User> getAll();
}
```

### Convenience methods

> Room provides convenience annotations for defining methods that perform simple inserts, updates, and deletes without requiring you to write a SQL statement.
If you need to define more complex inserts, updates, or deletes, or if you need to query the data in the database, use a query method instead.

**Insert**

```
@Dao
public interface UserDao {
    @Insert(onConflict = OnConflictStrategy.REPLACE)
    public void insertUsers(User... users);

    @Insert
    public void insertBothUsers(User user1, User user2);

    @Insert
    public void insertUsersAndFriends(User user, List<User> friends);
}
```

**Update**

```
@Dao
public interface UserDao {
    @Update
    public void updateUsers(User... users);
}
```

**Delete**

```
@Dao
public interface UserDao {
    @Delete
    public void deleteUsers(User... users);
}
```

