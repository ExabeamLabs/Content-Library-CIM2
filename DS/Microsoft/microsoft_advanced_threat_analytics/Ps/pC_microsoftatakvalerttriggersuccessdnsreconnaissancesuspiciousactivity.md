#### Parser Content
```Java
{
Name = "microsoft-ata-kv-alert-trigger-success-dnsreconnaissancesuspiciousactivity"
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|DnsReconnaissanceSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+? from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+\w))"""
  """\Wmsg=[^=]+? against (?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+\w))"""
  """\Wrequest=({malware_url}.+?)\s+(\w+=|$)"""
  """\Wshost=(?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```