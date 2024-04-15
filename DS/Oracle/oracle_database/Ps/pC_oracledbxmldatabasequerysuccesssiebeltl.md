#### Parser Content
```Java
{
Name = "oracle-db-xml-database-query-success-siebel-tl"
    Vendor = "Oracle"
    Product = "Oracle Database"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [
      "<sql_text>"
      "<db_user>"
    ]
    Fields = [
      "(?i)<Extended_Timestamp>({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d(:\\d\\d:\\d\\d.\\d+\\w+)?)"
      "(?i)<Userhost>({host}[^<]+)</Userhost>"
      "(?i)<DB_User>(\\/|({db_user}[^<]+))</DB_User>"
      "(?i)<OS_User>({user}[^<]+)</OS_User>"
      "(?i)<DBID>({db_id}\\d+)</DBID>"
      "(?i)<Object_Schema>({db_name}[^<]+)</Object_Schema>"
      "(?i)<Object_Name>({table_name}[^<]+)</Object_Name>"
      "(?i)<Sql_Text>({db_operation}(?!with|WITH)[^\\s]+)"
      "(?i)<Sql_Text>({db_query}.+?)\\s*</Sql_Text>"
    ]
    DupFields = [
      "db_user->account"
      "db_id->db_name"
    ]
    ParserVersion = "v1.0.0"
  

}
```