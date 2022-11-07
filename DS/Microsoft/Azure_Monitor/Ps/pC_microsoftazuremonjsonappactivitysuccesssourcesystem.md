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
    """SourceIp"+:"+({src_ip}[^"]+)""",
    """DestinationIp"+:"+({dest_ip}[^"]+)""",
    """DestinationPort"+:({dest_port}\d+)"""
    """"+Protocol"+:"+({protocol}[^"]+)""",
    """"+BytesSent"+:({bytes_out}\d+)""",
    """"+BytesReceived"+:({bytes_in}\d+)""",
    """"+Machine"+:"+({src_host}[^"]+)""",
    ]


}
```