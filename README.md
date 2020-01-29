# KotlinUtil

Kotlin utilities

..* Extension function stackTrace() for Exceptions
```java
println(e.stackTrace())
```

..* Manage multiple AutoCloseable resources 
```java
withResources {
  val connection = getConnection().use()
  val statement = connection.createStatement().use()
  val resultSet = statement.executeQuery(sql).use()
  while (resultSet.next()) { ... }
}
```

..* Cloned FTPClient from apache commons net so it is AutoCloseable (override `close()`) and can be automatically managed.
```java
withResources {
  val ftp = FTPClient(srcServer, srcPort, srcUser, srcPwd).use()
  ...
}
```



