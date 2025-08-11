#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-database-success-database
  Vendor = Google
  Product = Google Cloud Platform
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSZ" , "yyyy-MM-dd'T'HH:mm:ss.SSZ"]
  Conditions = [""""database_id":"""",  """"type":"cloudsql_database"""",""""project_id":"""","""dproc=Cloud PubSub"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"service_name":"({service_name}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"region":"({region}[^"]+)"""",
	  """STATEMENT:\s*({db_query}[^;]+)""",
	  """user\\?=({db_user}[^\s]+)""",
	  """db\\?=({db_name}[^\s,]+)"""
    """resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))""""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.logName,exa_field_name=log_name"""
    """exa_json_path=$..region,exa_field_name=region"""
    """exa_json_path=$..project_id,exa_field_name=project_id"""
    """exa_json_path=$..resource.type,exa_field_name=category"""
    """exa_json_path=$..timestamp,exa_field_name=time"""
    """exa_json_path=$..serviceName,exa_field_name=service_name"""
    """exa_regex="resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))"""",
    """exa_json_path=$..methodName,exa_field_name=operation""",
    """exa_json_path=$.protoPayload.request.statement,exa_field_name=db_query"""
    """exa_json_path=$.protoPayload.request.database,exa_field_name=db_name"""
    """exa_json_path=$.protoPayload.request.user,exa_field_name=db_user"""
  ]
  ParserVersion = v1.0.0


}
```