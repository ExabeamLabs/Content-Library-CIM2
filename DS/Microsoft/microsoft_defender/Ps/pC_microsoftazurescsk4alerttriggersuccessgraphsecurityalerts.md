#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-graphsecurityalerts
Vendor = Microsoft
Product = Microsoft Defender
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"vendor":"Microsoft""""
  """"provider":"ASC""""
  """"category":"ARM_UnusedAccountPersistence""""
  """PREVIEW - Suspicious management session using an inactive account detected"""
]
Fields = [
  """\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s"""
  """"eventDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"IP address\\":\\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"title":"({alert_name}[^"]+?)(\\u200b)?""""
  """"category":"({alert_type}[^"]+)""""
  """"severity":"({alert_severity}[^"]+)""""
  """"Identity address\\":\\"({account_name}[^@"\\]+)@({domain}[^"\\]+)"""
  """"description":"({event_name}[^"]+)""""
  """"Suspicious actions\\":\\"\[[\\"]+({additional_info}[^\]]+?)[\\""]+\]"""
]
ParserVersion = "v1.0.0"


}
```