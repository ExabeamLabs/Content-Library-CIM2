#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-handle-open-success-openremoteprocesshandle
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"cross_process"""", """"event.type":"Open Remote Process Handle"""" ]
  Fields = ${DLSentinelOneParsersTemplates.json-sentinelone-edr-events-dl.Fields} [
    """"agent.version":\s*"+({user_agent}[^"]+)"""",
    """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""",
    """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""",
    """"src.process.image.md5":\s*\\?"+({hash_md5}[^"\\]+)"""",
    """"src.process.pid":\s*({process_id}\d+)""",
    """"src.process.image.path":"({process_path}({process_dir}[^"]+?)[\\\/]*({process_name}[^"\\\/]+))\\*"""",

    """exa_json_path=$.['agent.version'],exa_field_name=user_agent""",
    """exa_json_path=$.['src.process.image.sha256'],exa_field_name=hash_sha256""",
    """exa_json_path=$.['src.process.image.sha1'],exa_field_name=hash_sha1""",
    """exa_json_path=$.['src.process.image.md5'],exa_field_name=hash_md5""",
    """exa_json_path=$.['src.process.pid'],exa_field_name=process_id""",
    """exa_json_path=$.['src.process.image.path'],exa_regex=({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))$"""
  ]

json-sentinelone-edr-events-dl = {
  Vendor = SentinelOne
  Product = "Singularity Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Fields = [
    """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"event\.type":"({event_name}[^"]+)""",
    """"endpoint\.name":"({dest_host}({host}[^"]+))""",
    """"task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """process\.name":"({process_name}[^"]+)""",
    """"endpoint.os":"({os}[^"]+)"""
    """"src.process.user":"((({domain}[^\\"]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"tgt.process.user":"((({dest_domain}[^\\"]+))\\+)?((({dest_user}Système|LOCAL SERVICE|NETWORK SERVICE|[^\\"$\s]+?)|({dest_user_full_name}[^"\s$]+\s[^"\s]+)))""""
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$..['event.type'],exa_field_name=event_name""",
    """exa_json_path=$..['endpoint.name'],exa_field_name=host""",
    """exa_json_path=$..['endpoint.name'],exa_field_name=dest_host""",
    """exa_regex="task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """exa_regex=process\.name":"({process_name}[^"]+)"""
    """exa_json_path=$..['endpoint.os'],exa_field_name=os"""
    """exa_json_path=$..['src.process.user'],exa_regex=((({domain}[^\\"$]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~\s]{1,40}\$?))($|")"""
    """exa_json_path=$..['tgt.process.user'],exa_regex=((({dest_domain}[^\\"$]+))\\+)?((({dest_user}Système|LOCAL SERVICE|NETWORK SERVICE|[^\\"$\s]+?)|({dest_user_full_name}[^"\s$]+\s[^"\s$]+)))($|")"""
    
}
```