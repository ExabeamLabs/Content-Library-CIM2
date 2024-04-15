#### Parser Content
```Java
{
Name = "oracle-db-xml-database-login-success-dbauth-tl"
    Vendor = "Oracle"
    Product = "Oracle Database"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Conditions = [
      "<db_user>"
      "<os_user>"
      "<userhost>"
      "<os_process>"
      "authenticated by:"
    ]
    Fields = [
      "(?i)<Extended_Timestamp>({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d+\\w)</Extended_Timestamp>"
      "(?i)<DB_User>(\\/|({db_user}.+?))</DB_User>"
      "(?i)<OS_User>({user}.+?)</OS_User>"
      "(?i)<Userhost>({src_host}[^\\<]+)</Userhost>"
      "(?i)<OS_Process>({process_id}\\d+)</OS_Process>"
      "(?i)<Session_Id>({session_id}\\d+)</Session_Id>"
      "(?i)<Returncode>({result}.+?)</Returncode>"
      "(?i)<DBID>({db_name}.+?)</DBID>"
      "(?i)PROTOCOL=({protocol}[^\\)]+)"
      "(?i)HOST=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)PORT=({src_port}\\d+)"
    ]
    DupFields = [
      "user->user"
      "db_user->account"
    ]
    ParserVersion = "v1.0.0"
  

}
```