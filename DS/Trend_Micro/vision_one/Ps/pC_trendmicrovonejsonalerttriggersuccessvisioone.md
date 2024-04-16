#### Parser Content
```Java
{
Name = trendmicro-vone-json-alert-trigger-success-visioone
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"app": "trendmicro""", """"workbenchName":""", """"type": "alert"""" ]
  Fields = [
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.app,exa_field_name=app""",
    """exa_json_path=$.type,exa_field_name=alert_type""",
    """exa_json_path=$.description,exa_field_name=alert_name""",
    """exa_json_path=$.createdTime,exa_field_name=time""",
    """exa_json_path=$.user,exa_field_name=user""",
    """exa_json_path=$.dest,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.detail.alertProvider,exa_field_name=alert_source""",
  ]


}
```