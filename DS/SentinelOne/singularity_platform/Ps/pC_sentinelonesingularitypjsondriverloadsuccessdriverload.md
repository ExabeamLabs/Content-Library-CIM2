#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-driver-load-success-driverload
  ParserVersion = "v1.0.0"
  Conditions = [""""dataSource.name":"SentinelOne"""",""""event.category":"driver"""",""""event.type":"Driver Load""""]
  Fields = ${DLSentinelOneParsersTemplates.json-sentinelone-edr-events.Fields} [
    """"agent.version":\s*"+({user_agent}[^"]+)"""",
    """"src.process.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^\\"]+))"""",
    """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""",
    """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""",
    """"src.process.image.md5":\s*\\?"+({hash_md5}[^"\\]+)"""",
    """"src.process.pid":\s*({process_id}\d+)""",
    """"src.process.image.path":"({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*"""",
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