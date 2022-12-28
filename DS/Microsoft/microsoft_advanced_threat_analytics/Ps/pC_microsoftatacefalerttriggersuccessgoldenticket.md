#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-success-goldenticket
Vendor = Microsoft
Product = Microsoft Advanced Threat Analytics
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|GoldenTicketSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[^\s]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```