#### Parser Content
```Java
{
Name = amazon-ards-json-database-success-databaseactivity
  Vendor = Amazon
  Product = Amazon RDS
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"type":"DatabaseActivityMonitoringRecord"""", """"instanceId":"""", """"databaseName":"""", """"dbUserName":"""" ]
  Fields = [
    """exa_json_path=$.databaseActivityEventList..logTime,exa_field_name=time""",
    """exa_json_path=$.databaseActivityEventList..command,exa_field_name=db_operation""",
    """exa_json_path=$.databaseActivityEventList..commandText,exa_field_name=db_query""",
    """exa_json_path=$.databaseActivityEventList..databaseName,exa_field_name=db_name""",
    """exa_json_path=$.databaseActivityEventList..dbUserName,exa_field_name=db_user""",
    """exa_json_path=$.databaseActivityEventList..objectName,exa_field_name=db_object""",
    """exa_json_path=$.databaseActivityEventList..engineNativeAuditFields.schema_name,exa_field_name=db_schema""",
    """exa_json_path=$.databaseActivityEventList,exa_regex="objectName":"({table_name}[^"]+)","objectType":"TABLE"""",
    """exa_json_path=$.databaseActivityEventList..serviceName,exa_field_name=service_name""",
    """exa_json_path=$.databaseActivityEventList..serverHost,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "db_user->user" ]


}
```