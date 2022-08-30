[<=== Back](../README.md)

# [Comparing Data Repositories](https://www.baeldung.com/spring-data-repositories)
*from Baeldung*

## Spring Data Repositories

- CrudRepository: provides CRUD functions
- PagingAndSortingRepository: provides methods to do pagination and sort records
- JpaRepository: provides JPA related methods such as flushing the persistence context and delete records in a batch

Because of the inheritance relationship, the JpaRepository contains the full API of CrudRepository and PagingAndSortingRepository.

Code Example: Find a Product based on its name:
```
@Repository
public interface ProductRepository extends JpaRepository<Product, Long> {
    Product findByName(String productName);
}
```

## CrudRepository

CrudRepository interface:
```
public interface CrudRepository<T, ID extends Serializable>
  extends Repository<T, ID> {

    <S extends T> S save(S entity);

    T findOne(ID primaryKey);

    Iterable<T> findAll();

    Long count();

    void delete(T entity);

    boolean exists(ID primaryKey);
}
```

Though simple, this interface provides all basic query abstractions needed in an application.

## PagingAndSortingRepository

PagingAndSortingRepository interface:
```
public interface PagingAndSortingRepository<T, ID extends Serializable> 
  extends CrudRepository<T, ID> {

    Iterable<T> findAll(Sort sort);

    Page<T> findAll(Pageable pageable);
}
```

## JpaRepository

JpaRepository interface:
```
public interface JpaRepository<T, ID extends Serializable> extends
  PagingAndSortingRepository<T, ID> {

    List<T> findAll();

    List<T> findAll(Sort sort);

    List<T> save(Iterable<? extends T> entities);

    void flush();

    T saveAndFlush(T entity);

    void deleteInBatch(Iterable<T> entities);
}
```

The JpaRepository extends the PagingAndSortingRepository, which extends the CrudRepository, meaning that it has all the methods available from both repositories.