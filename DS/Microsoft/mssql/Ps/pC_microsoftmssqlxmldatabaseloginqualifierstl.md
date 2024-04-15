#### Parser Content
```Java
{
Name = "microsoft-mssql-xml-database-login-qualifiers-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "MSSQL"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<event xmlns="
      "<provider name='mssql"
      "<keyword>audit "
    ]
    Fields = [
      "(?i)<TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<Provider Name ='({db_name}[^']+)'"
      "(?i)<Computer>({host}.+?)<\\/Computer>"
      "(?i)<EventData><Data>(({domain}[^\\\\\\/<>]+?)[\\\\\\/]+)?({user}[^\\\\\\/]+?)</Data>"
      "(?i)<Data>\\s*\\[CLIENT:\\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<Computer>({src_host}.+?)<\\/Computer>.*?<Data>\\s*\\[CLIENT:\\s*[^\\]]*?local machine"
      "(?i)<Data>\\s*\\[CLIENT:\\s*[^\\]]*?local machine.*?\\].*?<Computer>({src_host}.+?)<\\/Computer>"
      "(?i)Connection made using ({auth_package}[^.]+)."
      "(?i)<EventID Qualifiers=[^>]+>({event_code}\\d+)"
      "(?i)<Keyword>({result}Audit.+?)</Keyword>"
      "(?i)<Message>[^<>]*?Reason:\\s*({failure_reason}[^.]+?)\\."
      "(?i)\\sserver_principal_name:(({domain}[^\\\\]+)\\\\)?({user}[^\\s]+)\\sserver_principal_sid"
      "(?i)database_name:({db_name}[^\\s]+)"
      "(?i)\\Wserver_principal_name:(({domain}[^\\\\\\/]+?)[\\\\\\/])?({db_user}[^\\\\\\/\\s]+?)(\\s+\\w+:|\\s*$)"
      "(?i)\\Waction_id:({db_operation}[^\\s]+)"
      "(?i)schema_name:({db_schema}[^\\s]+)"
      "(?i)\\Wobject_name:({table_name}[^\\s]+)"
      "(?i)\\Wstatement:(|-- network|Login failed.+?|Network error code.+?|({db_query}.+?))(\\s+\\w+:|\\s*$)"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```