# Performance comparison of Android ORM Frameworks

At the moment there are a lot of ORM-libraries for the Android OS. We reviewed the most popular ones and compared them by performance and some other parameters.
As libraries for comparison, the most popular solutions at the time of writing were chosen: ORMLite, Sugar ORM, Freezer, DBFlow, requery, GreenDAO, ActiveAndroid, Room, Sprinkles. Also in the comparison participated "clean" SQLite - the built-in API for working with SQLite in Android, without the use of ORM, and the popular NoSql solution - Realm.

We considered 3 variants(simple, complex, balanced), and for each of them 4 operations(CRUD).
## Models
```java
public class Library{ 
    String address;
    String name;
}

public class Book{
    String author;
    String title;
    int pagesCount;
    int bookId; 
    Library library;
}
public class Person{
    String firstName;
    String secondName;
    Date birthdayDate;
    String gender;
    long phone;
    Library library;
}
```

## Test cases
* Simple - 1 Library object per 1000 Book objects 
* Complex - 1 Library object for 500 Book objects and 400 Person objects (5 Libraries, 2500 Books, 2000 Persons)
* Balanced - 1 Library object for 50 Book objects and 50 Person objects (50 Libraries, 2500 Books, 2500 Persons)

For each test cache/lazy initialization were turned off, and we perform an average of 10 measurements per operation.

## Results Table

## Histograms

#### Overall

#### More detailed (Simple)

#### More detailed (Complex)

#### More detailed (Balanced)

## Summary

##### DBFlow

##### Realm

##### GreenDao

##### Room


## Сonclusion

