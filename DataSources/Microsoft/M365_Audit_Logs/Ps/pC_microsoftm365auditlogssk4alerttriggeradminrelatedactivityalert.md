#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-sk4-alert-trigger-adminrelatedactivityalert
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = ["""dproc=Graph Security Alerts""", """"provider":"Office 365 Security and Compliance"""", """"title":"Admin Related Activity Alert"""", """"category":"Others"""" ]
  Fields = [
    """\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s""",
    """"eventDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"title":"({alert_name}[^"]+)"""",
    """"category":"({alert_type}[^"]+)"""",
    """"severity":"({alert_severity}[^"]+)"""",
    """"userPrincipalName":"({user}[^@"]+)@({email_domain}[^"]+)"""",
    """"accountName":"({user}[^"]+)"""",
    """"domainName":"({web_domain}[^"]+)"""",
    """"description":"({event_name}[^"]+)"""",
    """"comments":\["+({additional_info}[^\]]+?)"+\]"""
 ]


}
```