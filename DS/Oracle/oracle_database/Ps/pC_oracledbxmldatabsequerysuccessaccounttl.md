#### Parser Content
```Java
{
Name = "oracle-db-xml-databse-query-success-account-tl"
    Vendor = "Oracle"
    Product = "Oracle Database"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [
      "<db_user>"
      "<os_user>"
      "<userhost>"
      "<os_process>"
      "<dbid>"
      "<sql_text>"
    ]
    Fields = [
      "(?i)<Extended_Timestamp>({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d+\\w)</Extended_Timestamp>"
      "(?i)<DB_User>(\\/|({db_user}.+?))</DB_User>"
      "(?i)<OS_User>({user}.+?)</OS_User>"
      "(?i)<Userhost>({src_host}[^\\<]+)</Userhost>"
      "(?i)<OS_Process>({process_id}\\d+)</OS_Process>"
      "(?i)<Session_Id>({session_id}\\d+)</Session_Id>"
      "(?i)<Returncode>({result}.+?)</Returncode>"
      "(?i)PROTOCOL=({protocol}[^\\)]+)"
      "(?i)PORT=({src_port}\\d+)"
      "(?i)<DBID>({db_id}\\d+)</DBID>"
      "(?i)<Sql_Text>\\s*({db_query}({db_operation}\\w+)\\s.+?)\\s*</Sql_Text>"
    ]
    DupFields = [
      "user->user"
      "db_user->account"
      "db_id->db_name"
    ]
    ParserVersion = "v1.0.0"
  

}
```