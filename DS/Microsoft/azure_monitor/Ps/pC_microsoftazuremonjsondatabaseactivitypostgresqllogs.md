#### Parser Content
```Java
{
Name = microsoft-azuremon-json-database-activity-postgresqllogs
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [
    """destinationServiceName =Azure""",
    """"ServerType":"PostgreSQL"""",
    """"category":"PostgreSQLLogs""""
  ]
  Fields = [
    """exa_json_path=$.ServerType,exa_field_name=server_type""",
    """exa_json_path=$.ServerVersion,exa_field_name=server_version""",
    """exa_json_path=$.LogicalServerName,exa_field_name=server""",
    """exa_json_path=$.resourceId,exa_field_name=resource_id""",
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.Region,exa_field_name=region""",
    """exa_json_path=$.location,exa_field_name=location""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.properties.sqlerrcode,exa_field_name=failure_code""",
    """exa_json_path=$.properties.errorLevel,exa_field_name=severity""",
    """exa_json_path=$.properties.processId,exa_field_name=process_id""",
    """exa_json_path=$.properties.statement,exa_field_name=db_query""",
    """exa_json_path=$.properties.statement,exa_regex=^({db_operation}[^"\s]+)""",
    """exa_json_path=$.properties.message,exa_field_name=additional_info""",
    """exa_json_path=$.properties.client_ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$"""
  ]


}
```