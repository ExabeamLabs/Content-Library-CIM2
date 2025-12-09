#### Parser Content
```Java
{
Name = jamf-jamfpro-json-security-alerts-jamfprotect
  Vendor = "Jamf"
  Product = "Jamf Protect"
  ExtractionType = json
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [""""input":{""", """"eventType":"""", """"match":{""", """"facts":""", """"human":"""", """"related":"""  ]
  Fields = [
    """exa_json_path=$.input.eventType,exa_field_name=event_category""",
    """exa_json_path=$.input.host.hostname,exa_field_name=host""",
    """exa_json_path=$.input.host.ips[0],exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.input.host.os,exa_field_name=os_version""",
    """exa_json_path=$.input.host.serial,exa_field_name=serial_num""",
    """exa_json_path=$.input.match.actions[0].name,exa_field_name=action""",
    """exa_json_path=$.input.match.event.dev,exa_field_name=device_id""",
    """exa_json_path=$.input.match.event.eventID,exa_field_name=event_id""",
    """exa_json_path=$.input.match.event.gid,exa_field_name=group_id""",
    """exa_json_path=$.input.match.event.pid,exa_field_name=process_id""",
    """exa_json_path=$.input.match.event.timestamp,exa_field_name=time""",
    """exa_json_path=$.input.match.event.type,exa_field_name=operation_type""",
    """exa_json_path=$.input.match.facts[0].human,exa_field_name=alert_description""",
    """exa_json_path=$.input.match.facts[0].name,exa_field_name=alert_name""",
    """exa_json_path=$.input.match.facts[0].tags,exa_field_name=more_info""",
    """exa_json_path=$.input.match.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.input.related.binaries[0].sha1hex,exa_field_name=hash_sha1""",
    """exa_json_path=$.input.related.binaries[0].sha256hex,exa_field_name=hash_sha256""",
    """exa_json_path=$.input.related.binaries[0].signingInfo.appid,exa_field_name=app_id""",
    """exa_json_path=$.input.related.binaries[0].size,exa_field_name=bytes""",
    """exa_json_path=$.input.related.groups[0].name,exa_field_name=group_name""",
    """exa_json_path=$.input.related.processes[0].path,exa_regex=({process_path}({process_dir}[^"]+[\/]+)?({process_name}[^"]+))""",
    """exa_json_path=$.input.related.processes[0].ppid,exa_field_name=parent_process_id""",
    """exa_json_path=$.input.related.users[0].name,exa_regex=({user}[\w\.\-]{1,40}\$?)""",
    """exa_json_path=$.input.match.event.composedMessage,exa_field_name=additional_info""",
    """exa_json_path=$.input.match.event.name,exa_field_name=event_name""",
    """exa_json_path=$.input.match.event.targetpid,exa_field_name=dest_process_id""",
    """exa_json_path=$.input.related.files[0].sha1hex,exa_field_name=hash_sha1""",
    """exa_json_path=$.input.related.files[0].sha256hex,exa_field_name=hash_sha256""",
    """exa_json_path=$.input.related.files[0].path,exa_regex=({file_path}({file_dir}[^"]+[\/]+)?({file_name}[^"]+))""",
    """exa_json_path=$.input.match.event.path,exa_regex=({process_path}({process_dir}[^"]+[\/]+)?({process_name}[^"]+)),exa_match_expr=InList(toLower($.input.eventType), "gpgatekeeperevent")"""
  ]


}
```