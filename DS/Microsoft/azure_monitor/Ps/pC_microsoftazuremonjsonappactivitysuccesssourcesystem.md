#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-sourcesystem
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSZ"
  Conditions = [ """SourceSystem""", """src-endpoint""", """src-application-name""", """TenantId"""]
  Fields = [
# src_system is removed
# mg is removed
# counter_path is removed
# counter_name is removed
    """Direction"+:"+({direction}[^"]+)""",
    """ProcessName"+:"+({process_name}[^"]+)""",
    """SourceIp"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """DestinationIp"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """DestinationPort"+:({dest_port}\d+)"""
    """"+Protocol"+:"+({protocol}[^"]+)""",
    """"+BytesSent"+:({bytes_out}\d+)""",
    """"+BytesReceived"+:({bytes_in}\d+)""",
    """"+Machine"+:"+({src_host}[^"]+)""",
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.raw-event.TenantId,exa_field_name=tenant_id""",
    """exa_json_path=$.raw-event.Computer,exa_field_name=host""",
    """exa_json_path=$.raw-event.['$table'],exa_field_name=table""",
    """exa_json_path=$.raw-event.['_ResourceId'],exa_field_name=resource_id""",
    """exa_json_path=$.raw-event.ObjectName,exa_field_name=object""",
    """exa_json_path=$.src-application-name,exa_field_name=app""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_json_path=$.src-endpoint,exa_field_name=endpoint""",
    ]


}
```