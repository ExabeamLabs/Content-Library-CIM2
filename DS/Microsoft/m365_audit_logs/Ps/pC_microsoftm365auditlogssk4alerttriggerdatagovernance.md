#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-alert-trigger-datagovernance
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category":"DataGovernance"""", """"title":""", """"vendor":"Microsoft"""", """"provider":"Office 365 Security and Compliance"""" ]
  Fields = [
     """"eventDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
     """"id":\s*"({alert_id}[^"]+)"""",
     """"title":\s*"({alert_name}[^"]+?)(\\u200b)?"""",
     """"severity":\s*"({alert_severity}[^"]+)"""",
     """"category":\s*"({alert_type}[^"]+)"""",
     """"description":\s*"({additional_info}[^"]+)""""
  ]


}
```