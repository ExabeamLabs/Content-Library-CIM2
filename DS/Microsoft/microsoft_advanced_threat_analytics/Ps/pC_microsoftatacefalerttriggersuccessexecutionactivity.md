#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-success-executionactivity
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|RemoteExecutionSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]*?performed on ({host}\S+) from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))"""
  """\Wmsg=[^=]+?by (?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```