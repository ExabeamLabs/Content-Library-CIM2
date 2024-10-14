#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-success-bruteforceactivity
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|BruteForceSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({first_name}[\w\']+)\s+({last_name}\w+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+? from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
  """\d+:\d+:\d+.+?({dest_ip}\d+\.\d+\.\d+\.\d+).*?CEF:"""
]
ParserVersion = "v1.0.0"


}
```