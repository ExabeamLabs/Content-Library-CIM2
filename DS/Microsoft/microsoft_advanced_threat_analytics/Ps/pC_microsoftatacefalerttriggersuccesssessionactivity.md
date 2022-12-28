#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-success-sessionactivity
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|EnumerateSessionsSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+?performed by (?:(({last_name}[\w\']+), ({first_name}\w+))|({user}\w+))"""
  """\Wmsg=[^=]+?performed by .+?from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+)) against (?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+)),"""
  """\Wmsg=[^=]+? performed from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+\w)) against (?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+\w)).+? ({user}[^\s]+) \(.*?\)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[^\s]+))\s+(\w+=|$)"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```