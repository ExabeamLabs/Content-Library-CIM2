#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-graphsecurityalerts
Vendor = Microsoft
Product = Azure Security Center
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """dproc=Graph Security Alerts"""
  """"provider":"ASC""""
  """"category":"ARM_UnusedAccountPersistence""""
  """PREVIEW - Suspicious management session using an inactive account detected"""
]
Fields = [
  """\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s"""
  """"eventDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"IP address\\":\\"({src_ip}[A-Fa-f\d:.]+)"""
  """"title":"({alert_name}[^"]+)""""
  """"category":"({alert_type}[^"]+)""""
  """"severity":"({alert_severity}[^"]+)""""
  """"Identity address\\":\\"({account_name}[^@"\\]+)@({domain}[^"\\]+)"""
  """"description":"({event_name}[^"]+)""""
  """"Suspicious actions\\":\\"\[[\\"]+({additional_info}[^\]]+?)[\\""]+\]"""
]
ParserVersion = "v1.0.0"


}
```