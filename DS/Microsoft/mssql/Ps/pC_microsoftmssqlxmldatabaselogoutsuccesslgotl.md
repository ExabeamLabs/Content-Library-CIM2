#### Parser Content
```Java
{
Name = "microsoft-mssql-xml-database-logout-success-lgo-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "MSSQL"
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Conditions = [
      "action_id:lgo"
      "event_time:"
      "session_id:"
      "server_principal_id:"
    ]
    Fields = [
      "(?i)\\Wevent_time:({time}\\d+\\-\\d+\\-\\d+ \\d+:\\d+:\\d+\\.\\d{3})"
      "(?i)\\WUser=({user}[^\\s]+?)(\\s+\\w+=|\\s*$)"
      "(?i)\\WSid=({user_sid}[^\\s]+?)(\\s+\\w+=|\\s*$)"
      "(?i)\\Wserver_principal_name:(({domain}[^\\\\\\/]+?)[\\\\\\/])?({db_user}[^\\\\\\/\\s]+?)(\\s+\\w+:|\\s*$)"
      "(?i)\\Wserver_principal_sid:({db_user_sid}[^\\s]+)"
      "(?i)\\Wserver_instance_name:({dest_host}[^\\s]+)"
      "(?i)\\Wdatabase_name:({db_name}[^\\s]+)"
    ]
  

}
```