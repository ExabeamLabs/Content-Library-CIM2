#### Parser Content
```Java
{
Name = trendmicro-officescan-kv-alert-trigger-success-contentfiltering
Vendor = Trend Micro
Product = OfficeScan
TimeFormat = "M/dd/yyyy HH:mm:ss"
Conditions = [
  """TMCM:EVT_URL_CONTENT_FILTERING"""
]
Fields = [
  """\sEvent time \(local\)="({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)"""
  """({host}[\w.\-]+)\s+TMCM:({alert_type}\w+)"""
  """\sURL="({malware_url}[^"]+)"""
  """\sDestination IP="({dest_ip}[^"]+)"""
  """\sDomain="({domain}[^"]+)"""
  """\sClient host name="({src_host}[^"]+)"""
  """\sSource IP="({src_ip}[^"]+)"""
]
DupFields = [
  "alert_type->alert_name"
]
ParserVersion = "v1.0.0"


}
```