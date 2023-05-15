#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-registry-create-success-keycreate
ParserVersion = "v1.0.0"
Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"registry"""", """"event.type":"Registry Key Create""""]

json-sentinelone-singularityp-events = {
    Product = Singularity Platform
    Vendor = SentinelOne
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"event\.type":"({alert_name}[^"]+)""",
      """"event\.category":"({alert_type}[^"]+)"""",
      """"endpoint\.name":"({dest_host}[^"]+)""",
      """process\.name":"({process_name}[^"]+)""",
      """"endpoint.os":"({os}[^"]+)"""
      """"agent.version":\s*"+({user_agent}[^"]+)""""
      """"src.process.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^\\"]+))"""
      """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""
      """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""
      """"src.process.image.md5":\s*\\?"+({hash_md5}[^"\\]+)"""
      """"src.process.pid":\s*({process_id}\d+)"""
      """"src.process.image.path":"({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*""""
      """"registry.keyPath":"({object}({registry_path}({registry_key}[^"]+?)\\+({registry_value}[^"\\]+)))""""
    
}
```