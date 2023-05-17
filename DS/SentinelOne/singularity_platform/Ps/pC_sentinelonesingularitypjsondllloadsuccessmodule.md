#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-dll-load-success-module
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"i.scheme":"edr"""", """"event.category":"module"""", """"event.type":""" ]
  Fields = ${DLSentinelOneParsersTemplates.json-sentinelone-edr-events.Fields} [
    """"src\.process\.parent\.image\.path":"+\s*({parent_process}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
    """"src\.process\.image\.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """"src\.process\.pid":({process_id}\d+)""",
    """"src\.process\.cmdline":"({process_command_line}.+?)",""",
    """"event\.id":"({event_code}[^"]+)""",
    """"module.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """"module.sha1":"\s*"*({hash_sha1}[^"]+)"""
  ]
  DupFields = [ "host->dest_host"]

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
    
}
```