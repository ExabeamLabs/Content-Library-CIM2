#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-process-thread-create-success-remotethread
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"cross_process"""", """"event.type":"Remote Thread Creation"""" ]
  Fields = ${DLSentinelOneParsersTemplates.json-sentinelone-edr-events-dl.Fields} [
    """exa_json_path=$.['agent.version'],exa_field_name=user_agent""",
    """exa_regex="src.process.user":"*((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """exa_json_path=$.['src.process.image.sha256'],exa_field_name=hash_sha256""",
    """exa_json_path=$.['src.process.image.sha1'],exa_field_name=hash_sha1""",
    """exa_json_path=$.['src.process.image.md5'],exa_field_name=hash_md5""",
    """exa_json_path=$.['src.process.pid'],exa_field_name=process_id""",
    """exa_json_path=$.['src.process.image.path'],exa_regex=({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))$""",
  ]

json-sentinelone-edr-events-dl = {
  Vendor = SentinelOne
  Product = "Singularity Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Fields = [
    """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"event\.type":"({event_name}[^"]+)""",
    """"endpoint\.name":"({host}[^"]+)""",
    """"task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """process\.name":"({process_name}[^"]+)""",
    """"endpoint.os":"({os}[^"]+)"""
    """"src.process.user":"((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({domain}[^\\\s"]+))\\+)?(system|Système|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"tgt.process.user":"((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({dest_domain}[^\\\s"]+))\\+)?(system|Système|LOCAL SERVICE|(({dest_user}[^\\"$\s]+?)|({dest_user_full_name}[^"\s$]+\s[^"\s]+)))""""
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$..['event.type'],exa_field_name=event_name""",
    """exa_json_path=$..['endpoint.name'],exa_field_name=host""",
    """exa_regex"task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """exa_regex=process\.name":"({process_name}[^"]+)"""
    """exa_json_path=$..['endpoint.os'],exa_field_name=os"""
    """exa_json_path=$..['src.process.user'],exa_regex=((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({domain}[^\\\s"$]+))\\+)?(system|Système|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))($|")"""
    """exa_json_path=$..['tgt.process.user'],exa_regex=((NT AUTHORITY|NT-AUTORITAT|AUTORITE NT|({dest_domain}[^\\\s"$]+))\\+)?(system|Système|LOCAL SERVICE|(({dest_user}[^\\"$\s]+?)|({dest_user_full_name}[^"\s$]+\s[^"\s$]+)))($|")"""
    
}
```