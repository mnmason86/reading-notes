[<=== Back](../README.md)

# Hibernate Many to Many

### Entity relationships

Entity relationship diagram showing a 'many-to-many' association between the entities *employee* and *project*

![Relationship Diagram](https://www.baeldung.com/wp-content/uploads/2017/09/New.png)

- Employees can be assigned to multiple projects
- Projects can have multiple assigned employees
- A **join table** *employee_project* is required to connect both sides

### Table Creation

Assuming the database is already set up, here is the creation of the three required tables:

```
CREATE TABLE `employee` (
  `employee_id` int(11) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(50) DEFAULT NULL,
  `last_name` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`employee_id`)
) ENGINE=InnoDB AUTO_INCREMENT=17 DEFAULT CHARSET=utf8;

CREATE TABLE `project` (
  `project_id` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`project_id`)
) ENGINE=InnoDB AUTO_INCREMENT=18 DEFAULT CHARSET=utf8;

CREATE TABLE `employee_project` (
  `employee_id` int(11) NOT NULL,
  `project_id` int(11) NOT NULL,
  PRIMARY KEY (`employee_id`,`project_id`),
  KEY `project_id` (`project_id`),
  CONSTRAINT `employee_project_ibfk_1` 
   FOREIGN KEY (`employee_id`) REFERENCES `employee` (`employee_id`),
  CONSTRAINT `employee_project_ibfk_2` 
   FOREIGN KEY (`project_id`) REFERENCES `project` (`project_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```


### Model Classes

In the *employee* and *project* models, each must refer to the other with the `@ManyToMany` annotation

```
@Entity
@Table(name = "Employee")
public class Employee { 
    // ...
 
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();
   
    // standard constructor/getters/setters
}
```
```
@Entity
@Table(name = "Project")
public class Project {    
    // ...  
 
    @ManyToMany(mappedBy = "projects")
    private Set<Employee> employees = new HashSet<>();
    
    // standard constructors/getters/setters   
}
```

