#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-dll-load-success-module
  ParserVersion = "v1.0.0"
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"module"""", """"event.type":""" ]
  Fields = ${DLSentinelOneParsersTemplates.json-sentinelone-edr-events-dl.Fields} [
    """"src\.process\.parent\.image\.path":"+\s*({parent_process_path}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
    """"src\.process\.image\.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """"src\.process\.pid":({process_id}\d+)""",
    """"src\.process\.cmdline":"({process_command_line}.+?)",""",
    """"event\.id":"({event_code}[^"]+)""",
    """"module.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """"module.sha1":"\s*"*({hash_sha1}[^"]+)"""
    """exa_regex="src\.process\.parent\.image\.path":"+\s*({parent_process_path}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
    """exa_regex="src\.process\.image\.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """exa_json_path=$..['src.process.pid'],exa_field_name=process_id""",
    """exa_json_path=$..['src.process.cmdline'],exa_field_name=process_command_line""",
    """exa_json_path=$..['event.id'],exa_field_name=event_code""",
    """exa_regex="module.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """exa_json_path=$..['module.sha1'],exa_field_name=hash_sha1""",
  ]
  DupFields = [ "host->dest_host"]

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
    """"src.process.user":"((({domain}[^\\"]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"tgt.process.user":"((({dest_domain}[^\\"]+))\\+)?((({dest_user}Système|LOCAL SERVICE|NETWORK SERVICE|[^\\"$\s]+?)|({dest_user_full_name}[^"\s$]+\s[^"\s]+)))""""
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$..['event.type'],exa_field_name=event_name""",
    """exa_json_path=$..['endpoint.name'],exa_field_name=host""",
    """exa_regex"task\.path":"({file_path}({file_dir}[^"]*?)({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
    """exa_regex=process\.name":"({process_name}[^"]+)"""
    """exa_json_path=$..['endpoint.os'],exa_field_name=os"""
    """exa_json_path=$..['src.process.user'],exa_regex=((({domain}[^\\"$]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~\s]{1,40}\$?))($|")"""
    """exa_json_path=$..['tgt.process.user'],exa_regex=((({dest_domain}[^\\"$]+))\\+)?((({dest_user}Système|LOCAL SERVICE|NETWORK SERVICE|[^\\"$\s]+?)|({dest_user_full_name}[^"\s$]+\s[^"\s$]+)))($|")"""
    
}
```