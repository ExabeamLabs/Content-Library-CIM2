#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-documentdb
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ExtractionType = json
  Conditions = [ """"resourceId":""", """"category":""", """MICROSOFT.DOCUMENTDB""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$..address,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.operationName,exa_field_name=db_operation""",
    """exa_json_path=$..databaseName,exa_field_name=db_name""",
    """exa_json_path=$..collectionName,exa_field_name=table_name""",
    """exa_json_path=$..userAgent,exa_field_name=user_agent""",
    """exa_regex=({app}MICROSOFT\.DOCUMENTDB)""",
    """exa_json_path=$..category,exa_field_name=category""",
    """exa_json_path=$.resourceId,exa_field_name=resource""",
    """exa_json_path=$..duration,exa_field_name=duration""",
    """exa_json_path=$..activityId,exa_field_name=activity_id"""
  ]
  ParserVersion = v1.0.0


}
```