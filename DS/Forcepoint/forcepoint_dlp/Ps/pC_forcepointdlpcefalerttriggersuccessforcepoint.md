#### Parser Content
```Java
{
Name = "forcepoint-dlp-cef-alert-trigger-success-forcepoint"
Vendor = "Forcepoint"
Product = "Forcepoint DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint CASB|"""
  """sourceServiceName ="""
]
Fields = [
  """CEF:([^\|]*\|){2}({alert_type}[^\|]+)\|[^\|]*\|({alert_id}[^\|]+)\|[^\|]*\|({alert_severity}[^\|]+)\|"""
  """\Wrt=({time}\d{13})"""
  """\Wcs1=({alert_name}.+?)\s+(\w+=|$)"""
  """\Wduser=({email_address}[^@=]+[^\.]+\.[^=]+)\s+(\w+=|$)"""
  """\Wsuser=({user}.+?)\s+(\w+=|$)"""
  """\Wact=({result}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```