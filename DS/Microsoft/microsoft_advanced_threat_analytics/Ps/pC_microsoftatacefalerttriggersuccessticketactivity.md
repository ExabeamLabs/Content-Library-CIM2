#### Parser Content
```Java
{
Name = microsoft-ata-cef-alert-trigger-success-ticketactivity
Vendor = "Microsoft"
Product = "Microsoft Advanced Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """|Microsoft|ATA|"""
  """|PassTheTicketSuspiciousActivity|"""
]
Fields = [
  """CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\WexternalId=({alert_id}\d+)"""
  """\Wstart=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\Wsuser=(?:(({last_name}[\w\']+), ({first_name}\w+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)"""
  """\Wapp=({service_name}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\Wmsg=[^=]+?from (?:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w.\-]+)) to (?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""
  """\Wmsg=[^=]+?access (\w+\/)?({malware_url}\S+[^\s\.])"""
  """\Wshost=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```