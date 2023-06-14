#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-database-activity-postgresqllogs
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ParserVersion = v1.0.0
  Conditions=[
    """CEF""",
    """MICROSOFT.DBFORPOSTGRESQL""",
    """"category":"PostgreSQLLogs"""",
    """"message":"""
  ]
  Fields=[
     """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
     """ResourceGroup":"({server_group}[^"]+)""",
     """schemaName":"({db_schema}[^"]+)""",
     """"message":"({db_operation}[^"]+)""",
     """"tableName":"({table_name}[^"]+)""",
     """"detail":"({additional_info}[^"]+)""",
     """"LogicalServerName":"({server}[^"]+)""",
# azure_resource_id is removed
     """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*[\];]""",
     """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]""",
     """category":"({category}[^"]+)"""",
     """protocol\\=({protocol}[^,]+)""",
     """cipher\\=({cipher}[^,]+)""",
     """"+domain"+:"+({domain}[^"]+)"""
     """"resourceId":\s*"({object}[^"]{1,249})"""
     """\WdestinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
     """"operationName":"({operation}[^"]+)"""
  ]
  DupFields= ["event_hub_namespace->host", "object->resource" , "db_operation->additional_info"]


}
```