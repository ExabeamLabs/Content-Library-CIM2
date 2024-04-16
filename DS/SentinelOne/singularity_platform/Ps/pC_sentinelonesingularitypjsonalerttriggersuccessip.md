#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-alert-trigger-success-ip
Product = Singularity Platform
Vendor = SentinelOne
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ParserVersion = "v1.0.0"
Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"ip"""", """"event.type":"IP Connect""""]
Fields = [
  """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
  """"dst.ip.address":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"src.ip.address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"src.port.number":\s*({src_port}\d+)"""
  """"dst.port.number":\s*({dest_port}\d+)"""
  """"event\.type":"({event_name}[^"]+)"""
  """"endpoint\.name":"({host}[^"]+)"""
  """process\.name":"({process_name}[^"]+)""",
  """"endpoint.os":"({os}[^"]+)"""
  """"agent.version":\s*"+({user_agent}[^"]+)""""
  """"src.process.user":"*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+?))""""
  """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""
  """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""
  """"src.process.image.md5":\s*\\?"+({hash_md5}[^"\\]+)"""
  """"src.process.pid":\s*({process_id}\d+)"""
  """"src.process.image.path":"({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*""""
  """"endpoint.type":"({host_type}[^"]+)"""
  """"event.network.connectionStatus":"({result}[^"]+)"""
  ]
  DupFields = [ "host->dest_host"]


}
```