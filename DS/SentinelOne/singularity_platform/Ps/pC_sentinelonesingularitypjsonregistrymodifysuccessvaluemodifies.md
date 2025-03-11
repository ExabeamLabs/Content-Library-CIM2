#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-registry-modify-success-valuemodifies
ParserVersion = "v1.0.0"
Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"registry"""", """"event.type":"Registry Value Modified""""]
DupFields = [ "host->dest_host", "alert_name->event_name" ]
Fields = ${SentinelOneParsersTemplates.json-sentinelone-singularityp-events.Fields}[
  """exa_json_path=$..['registry.value'],exa_field_name=registry_details""",
  """exa_json_path=$..['registry.valueType'],exa_field_name=registry_details_type"""
]

json-sentinelone-singularityp-events = {
    Product = Singularity Platform
    Vendor = SentinelOne
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields = [
      """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"event\.type":"({alert_name}[^"]+)""",
      """"event\.category":"({alert_type}[^"]+)"""",
      """"endpoint\.name":"({host}[^"]+)""",
      """process\.name":"({process_name}[^"]+)""",
      """"endpoint.os":"({os}[^"]+)"""
      """"agent.version":\s*"+({user_agent}[^"]+)""""
      """"src.process.user":"*((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({domain}[^\\"\s]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
      """"tgt.process.user":"((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({dest_domain}[^\\"\s]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|({dest_user}[^"]+?))"""",
      """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""
      """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""
      """"src.process.image.md5":\s*\\?"+({hash_md5}[^"\\]+)"""
      """"src.process.pid":\s*({process_id}\d+)"""
      """"src.process.image.path":"({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*""""
      """"registry.value":"({registry_value}[^"]+)""",
      """"registry.keyPath":"({object}({registry_path}({registry_key}[^"]+?)\\+({registry_value}[^"\\]+)))"""",
      """event\.name":"({operation}[^"]+)"""",
      """"endpoint\.type":"({host_type}[^"]+)"""
      """exa_json_path=$..timestamp,exa_field_name=time"""
      """exa_json_path=$..['event.type'],exa_field_name=alert_name"""
      """exa_json_path=$..['event.category'],exa_field_name=alert_type"""
      """exa_json_path=$..['endpoint.name'],exa_field_name=host"""
      """exa_regex=process\.name":"({process_name}[^"]+)"""
      """exa_json_path=$..['endpoint.os'],exa_field_name=os"""
      """exa_json_path=$..['agent.version'],exa_field_name=user_agent"""
      """exa_regex="src.process.user":"*((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
      """exa_json_path=$..['tgt.process.user'],exa_regex=((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({dest_domain}[^\\"\s]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|Système|({dest_user}[^"\s$]+?))$""",
      """exa_json_path=$..['src.process.image.sha256'],exa_field_name=hash_sha256"""
      """exa_json_path=$..['src.process.image.sha1'],exa_field_name=hash_sha1"""
      """exa_json_path=$..['src.process.image.md5'],exa_field_name=hash_md5"""
      """exa_json_path=$..['src.process.pid'],exa_field_name=process_id"""
      """exa_regex="src.process.image.path":"({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*""""
      """exa_json_path=$..['registry.value'],exa_field_name=registry_value"""
      """exa_regex="registry.keyPath":"({object}({registry_path}({registry_key}[^"]+?)\\+({registry_value}[^"\\]+)))"""",
      """exa_regex=event\.name":"({operation}[^"]+)"""",
      """exa_json_path=$..['endpoint.type'],exa_field_name=host_type"""
    
}
```