# KotlinUtil

Kotlin utilities

Extension stackTrack() for Exceptions
`
e.stackTrack()
`

Manage multiple autocloseable resources 
`
withResources {
  val connection = getConnection().use()
  val statement = connection.createStatement().use()
  val resultSet = statement.executeQuery(sql).use()
  while (resultSet.next()) { ... }
}
`



