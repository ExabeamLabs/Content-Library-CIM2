#### Parser Content
```Java
{
Name = sentinelone-singularityp-json-process-create-success-process
  ExtractionType = json
  ParserVersion = v1.0.0
  Conditions = [ """"dataSource.name":"SentinelOne"""", """"event.category":"process"""", """"event.type":"Process Creation"""" ]
  Fields = ${SentinelOneParsersTemplates.json-sentinelone-edr-events.Fields} [
    """"endpoint.type":"({device_type}[^"]+)"""",
    """"src.process.image.sha256":\s*\\?"+({hash_sha256}[^"\\]+)"""",
    """"src.process.image.sha1":\s*\\?"+({hash_sha1}[^"\\]+)"""",
    """"src.process.user":"*((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+?))"""",
    """"src.process.parent.image.path":"+\s*({parent_process_path}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))"""",
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
    """tgt.process.name":"({process_name}[^"]+)""""
    """src.process.name":"({parent_process_name}[^"]+)""""
    """"src.process.parent.name":"({grandparent_process_path}[^"]+)"""
    """tgt.process.user":"*((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"\s]+?)|({full_name}[^"]+))""""

    """exa_json_path=$.['endpoint.type'],exa_field_name=device_type""",
    """exa_json_path=$.['src.process.image.sha256'],exa_field_name=hash_sha256""",
    """exa_json_path=$.['src.process.image.sha1'],exa_field_name=hash_sha1""",
    """exa_regex="src.process.user":"*((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+?))""""
    """exa_json_path=$.['src.process.parent.image.path'],exa_regex=({parent_process_path}({parent_process_dir}[^@]+?)[\\\/]*({parent_process_name}[^"\\\/]+))$""",
    """exa_regex=process.image.path":"({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))"""",
    """exa_json_path=$.['src.process.image.path'],exa_regex=({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))$""",
    """exa_json_path=$.['tgt.process.image.path'],exa_regex=({dest_process_path}({dest_process_dir}(:?[\w:]+)?[^"]*\\)({dest_process_name}[^"]+))$""",
    """exa_json_path=$.['src.process.pid'],exa_field_name=process_id""",
    """exa_regex=process.cmdline":"[\\]*({process_command_line}.+?)"""",
    """exa_json_path=$.['src.process.cmdline'],exa_field_name=process_command_line""",
    """exa_json_path=$.['src.process.parent.cmdline'],exa_field_name=parent_process_command_line""",
    """exa_json_path=$.['tgt.process.publisher'],exa_field_name=dest_process_publisher""",
    """exa_json_path=$.['src.process.publisher'],exa_field_name=process_publisher""",
    """exa_json_path=$.['src.process.parent.publisher'],exa_field_name=parent_process_publisher""",
    """exa_json_path=$.['tgt.process.name'],exa_field_name=process_name""",
    """exa_json_path=$.['src.process.name'],exa_field_name=parent_process_name""",
    """exa_json_path=$.['src.process.parent.name'],exa_field_name=grandparent_process_path""",
    """exa_regex="tgt.process.user":"*((NT AUTHORITY|NT-AUTORITÄT|({domain}[^\\"]+))[\\\/]+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"\s]+?)|({full_name}[^"]+))""""
  ]
  DupFields = [ "host->dest_host" ]

json-sentinelone-edr-events = {
    Vendor = SentinelOne
    Product = "Singularity Platform"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    ExtractionType = json
    Fields = [
      """"timestamp":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
      """"event\.type":"({event_name}[^"]+)""",
      """"endpoint\.name":"({host}[^"]+)""",
      """"task\.path":"({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
      """process\.name":"({process_name}[^"]+)""",
      """"endpoint.os":"({os}[^"]+)""",
      """"event\.category":"({additional_info}[^"]+)"""",
      """"endpoint\.type":"({host_type}[^"]+)"""
      """"src\.process\.pid":({process_id}\d+)""",
      """"src\.process\.cmdline":"({process_command_line}.+?)",""",
      """"account\.id":"({account_id}[^"]+)""",
      """exa_json_path=$..timestamp,exa_field_name=time""",
      """exa_json_path=$..['event.type'],exa_field_name=event_name""",
      """exa_json_path=$..['endpoint.name'],exa_field_name=host""",
      """exa_regex="task\.path":"({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\"]+?(\.({file_ext}[^\\."]+?))?))"""",
      """exa_json_path=$..['src.process.name'],exa_field_name=process_name""",
      """exa_json_path=$..['endpoint.os'],exa_field_name=os""",
      """exa_json_path=$..['event.category'],exa_field_name=additional_info""",
      """exa_json_path=$..['endpoint.type'],exa_field_name=host_type""",
      """exa_json_path=$..['src.process.pid'],exa_field_name=process_id""",
      """exa_json_path=$..['src.process.cmdline'],exa_field_name=process_command_line""",
      """exa_json_path=$..['account.id'],exa_field_name=account_id"""
    
}
```