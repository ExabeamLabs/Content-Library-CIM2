#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-sourcesystem
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSZ"
  Conditions = [ """SourceSystem""", """src-endpoint""", """src-application-name""", """TenantId"""]
  Fields = [
    """"+time"+:"+({time}[^"]+)""",
    """"+TenantId"+:"+({tenant_id}[^"]+)""",
# src_system is removed
    """"+Computer"+:"+({host}[^"]+)""",
    """"+\$table"+:"+({table}[^"]+)""",
    """"+_ResourceId"+:"+({resource_id}[^"]+)""",
# mg is removed
    """"+ObjectName"+:"+({object}[^"]+)""",
# counter_path is removed
    """"+src-application-name"+:"+({app}[^"]+)""",
# counter_name is removed
    """"+src-account-name"+:"+({account_name}[^"]+)""",
    """"+src-endpoint"+:"+({endpoint}[^"]+)""",
    """Direction"+:"+({direction}[^"]+)""",
    """ProcessName"+:"+({process_name}[^"]+)""",
    """SourceIp"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """DestinationIp"+:"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """DestinationPort"+:({dest_port}\d+)"""
    """"+Protocol"+:"+({protocol}[^"]+)""",
    """"+BytesSent"+:({bytes_out}\d+)""",
    """"+BytesReceived"+:({bytes_in}\d+)""",
    """"+Machine"+:"+({src_host}[^"]+)""",
    ]


}
```