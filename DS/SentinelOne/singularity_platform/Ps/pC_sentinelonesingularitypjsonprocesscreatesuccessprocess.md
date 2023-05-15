#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-process-create-success-process
  ParserVersion = v1.0.0
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"process"""", """"event.type":"Process Creation"""", """"endpoint.os":"windows"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-edr-events.Fields} [
    """"endpoint.type":"({device_type}[^"]+)"""",
    """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""",
    """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""",
    """"src.process.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^\\"]+))"""",
    """"src.process.parent.image.path":"+\s*({parent_process}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
    """"src.process.image.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """"src.process.pid":({process_id}\d+)""",
    """"src.process.cmdline":"({process_command_line}.+?)",""",
  ]

json-sentinelone-edr-events = {
    Vendor = SentinelOne
    Product = "Singularity Platform"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"event\.type":"({event_name}[^"]+)""",
      """"endpoint\.name":"({dest_host}[^"]+)""",
      """"task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
      """process\.name":"({process_name}[^"]+)""",
      """"endpoint.os":"({os}[^"]+)"""
    
}
```