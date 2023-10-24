#### Parser Content
```Java
{
Name = "microsoft-mssql-json-database-activity-success-dbactivity"
  Vendor = "Microsoft"
  Product = "MSSQL"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """"class_type": """", """"statement":""", """"database_name":""", """"action_id":""" ]
  Fields = [
        """"server_instance_name":\s*"({host}[\w.-]+)"""",
        """"action_id":\s*"({db_operation}\w+)\s*"""",
        """"event_time":\s*"({time}\d{4}-\d{2}-\d{2} (\d{2}:){2}\d{2}\.\d{3})""",
        """"server_principal_name":\s*"(({domain}[^\\"]+?)[\\]{1,2})?({db_user}[^\s"]+?)"""",
        """"database_name":\s*"({db_name}[^"]+)"""",
        """"schema_name":\s*"({db_schema}[^"]+)"""",
        """"object_name":\s*"({db_object}[^"]+)"""",
        """"statement":\s*"({db_query}[^"]+)""""
        """"client_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
        """"host_name":\s*"({src_host}[^"]+)""""
  ]
  DupFields = [ "db_user->user" ]
  ParserVersion = "v1.0.0"


}
```