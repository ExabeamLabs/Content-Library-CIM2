#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-process-create-success-process
  ParserVersion = v1.0.0
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"process"""", """"event.type":"Process Creation"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-edr-events.Fields} [
    """"endpoint.type":"({device_type}[^"]+)"""",
    """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""",
    """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""",
    """"src.process.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))"""",
    """"src.process.parent.image.path":"+\s*({parent_process}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
    """process.image.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))""""
    """"src.process.image.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """"tgt.process.image.path":"({dest_process_path}({dest_process_dir}(:?[\w:]+)?[^"]*\\)({dest_process_name}[^"]+))"""",
    """"src.process.pid":({process_id}\d+)""",
    """process.cmdline":"[\\]*({process_command_line}.+?)","""
    """"src.process.cmdline":"({process_command_line}.+?)",""",
    """"src.process.parent.cmdline":"({parent_process_command_line}.+?)","""
    """"tgt.process.publisher":"({dest_process_publisher}[^"]+)""""
    """"src.process.publisher":"({process_publisher}[^"]+)""""
    """"src.process.parent.publisher":"({parent_process_publisher}[^"]+)""""
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