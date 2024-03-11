#### Parser Content
```Java
{
Name = oracle-db-xml-database-query-success-siebel
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """<Sql_Text>"""
  """<DB_User>"""
]
Fields = [
  """<Extended_Timestamp>({time}\d\d\d\d-\d\d-\d\dT\d\d(:\d\d:\d\d.\d+\w+)?)"""
  """<Userhost>({src_host}[^<]+)</Userhost>"""
  """<DB_User>(\/|({db_user}[^<]+))</DB_User>"""
  """<OS_User>({user}[^<]+)</OS_User>"""
  """<DBID>({db_id}\d+)</DBID>"""
  """<Object_Schema>({db_name}[^<]+)</Object_Schema>"""
  """<Object_Name>({table_name}[^<]+)</Object_Name>"""
  """<Sql_Text>({db_operation}(?!with|WITH)[^\s]+)"""
  """<Sql_Text>({db_query}.+?)\s*</Sql_Text>"""
]
DupFields = [
  "db_user->account"
  "db_id->db_name"
]
ParserVersion = "v1.0.0"


}
```