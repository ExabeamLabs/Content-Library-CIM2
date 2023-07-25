#### Parser Content
```Java
{
Name = amazon-ards-json-database-success-databaseactivity
  Vendor = Amazon
  Product = Amazon RDS
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
  Conditions = [ """"type":"DatabaseActivityMonitoringRecord"""", """"instanceId":"""", """"databaseName":"""", """"dbUserName":"""" ]
  Fields = [
    """"logTime":"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2}\.\d{7})""",
    """"command":"({db_operation}[^"]+)"""",
    """"commandText":"({db_query}[^"]+)"""",
    """"databaseName":"({db_name}[^"]+)"""",
    """"dbUserName":"({db_user}[^"]+)"""",
    """"objectName":"({db_object}[^"]+)"""",
    """"schema_name":"({db_schema}[^"]+)"""",
    """"objectName":"({table_name}[^"]+)","objectType":"TABLE"""",
    """"serviceName":"({service_name}[^"]+)"""",
    """"serverHost":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  ]
  DupFields = [ "db_user->user" ]


}
```