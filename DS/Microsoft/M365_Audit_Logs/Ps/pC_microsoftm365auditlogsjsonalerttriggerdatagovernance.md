#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-alert-trigger-datagovernance
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category": "DataGovernance"""", """"title": """, """"vendor": "Microsoft"""", """"provider": "Office 365 Security and Compliance"""" ]
  Fields = [
     """"id":\s*"({alert_id}[^"]+)"""",
     """"title":\s*"({alert_name}[^"]+)"""",
     """"severity":\s*"({alert_severity}[^"]+)"""",
     """"category":\s*"({alert_type}[^"]+)"""",
     """"description":\s*"({additional_info}[^"]+)"""",
     """"eventDateTime":\s*"({time}[^"]+)""""
    ]


}
```