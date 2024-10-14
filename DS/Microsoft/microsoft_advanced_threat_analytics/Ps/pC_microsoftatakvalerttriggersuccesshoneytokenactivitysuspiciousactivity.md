#### Parser Content
```Java
{
Name = "microsoft-ata-kv-alert-trigger-success-honeytokenactivitysuspiciousactivity"
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|HoneytokenActivitySuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+?performed by .+?(login to| from) (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))"""
]
ParserVersion = "v1.0.0"


}
```