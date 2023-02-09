#### Parser Content
```Java
{
Name = microsoft-mcas-cef-alert-trigger-success-siemagent
Vendor = "Microsoft"
Product = "Microsoft CAS"
TimeFormat = "epoch"
Conditions = [
  """|MCAS|SIEM_Agent|"""
  """CEF:"""
  """|ALERT_"""
]
Fields = [
  """({host}[\w\-\.]+)\s+CEF:"""
  """\Wrt=({time}\d{13})"""
  """CEF:([^\|]*?\|){4}({alert_name}[^\|]+?)\|"""
  """CEF:([^\|]*?\|){5}({alert_type}[^\|]+?)\|"""
  """CEF:([^\|]*?\|){6}({alert_severity}\d+)"""
  """\WexternalId=({alert_id}[^\s]+)\s+(\w+=|$)"""
  """\Wsuser=({email_address}[^\s]+)\s+(\w+=|$)"""
  """\Wcs1=({additional_info}.+?)\s+(\w+=|$)"""
  """DestinationServiceName =({process_name}.*?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```