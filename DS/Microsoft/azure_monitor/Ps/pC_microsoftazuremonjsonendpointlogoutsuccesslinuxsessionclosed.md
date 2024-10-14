#### Parser Content
```Java
{
Name = microsoft-azuremon-json-endpoint-logout-success-linuxsessionclosed
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions= [ """"Type":"Syslog"""", """ session closed for user """, """"SourceSystem":"Linux"""", """"SyslogMessage":""", """"Facility":"authpriv""""]
  Fields = [
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_json_path=$.Type,exa_field_name=event_category""",
    """exa_json_path=$.ProcessName,exa_field_name=process_name""",
    """exa_json_path=$.ProcessID,exa_field_name=$.ProcessID""",
    """exa_json_path=$.TenantId,exa_field_name=tenant_id""",
    """exa_json_path=$.Computer,exa_field_name=src_host""",
    """exa_json_path=$.CollectorHostName,exa_field_name=host""",
    """exa_json_path=$.SourceSystem,exa_field_name=os""",
    """exa_json_path=$.SyslogMessage,exa_field_name=additional_info""",
    """exa_json_path=$.SeverityLevel,exa_field_name=severity""",
    """exa_regex=(({event_name}session closed for user)\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
  ]


}
```