#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-dns-request-fail-dnsunresolved
  ParserVersion = v1.0.0
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"i.scheme":"edr"""", """"event.category":"dns"""", """"event.type":"DNS Unresolved"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-edr-events.Fields} [
    """"src.process.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))"""",
    """"endpoint.type":"({device_type}[^"]+)"""",
    """"src.process.parent.image.path":"+\s*({parent_process}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
    """"src.process.image.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """"src.process.pid":({process_id}\d+)""",
    """"src.process.cmdline":"({process_command_line}.+?)","""",
    """"event.dns.request":"({dns_query}[^"]+)"""",
  ]
  DupFields = [ "host->dest_host" ]

json-sentinelone-edr-events = {
    Vendor = SentinelOne
    Product = "Singularity Platform"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"event\.type":"({event_name}[^"]+)""",
      """"endpoint\.name":"({host}[^"]+)""",
      """"task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
      """process\.name":"({process_name}[^"]+)""",
      """"endpoint.os":"({os}[^"]+)""",
      """"event\.category":"({additional_info}[^"]+)"""",
      """"endpoint\.type":"({host_type}[^"]+)"""
      """"src\.process\.pid":({process_id}\d+)""",
      """"src\.process\.cmdline":"({process_command_line}.+?)",""",
      """"account\.id":"({account_id}[^"]+)""",
    
}
```