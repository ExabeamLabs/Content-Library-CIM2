#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-alert-trigger-supervision
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category":""", """"Supervision"""", """"title":""", """"vendor":""",  """"Microsoft"""", """"provider":""",  """"Office 365 Security and Compliance"""" ]
  Fields = [
     """exa_json_path=$.id,exa_field_name=alert_id""",
     """exa_json_path=$.title,exa_field_name=alert_name""",
     """exa_json_path=$.severity,exa_field_name=alert_severity""",
     """exa_json_path=$.category,exa_field_name=alert_type""",
     """exa_json_path=$.description,exa_field_name=additional_info""",
     """exa_json_path=$.eventDateTime,exa_field_name=time""",
  ]


}
```