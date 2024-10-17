#### Parser Content
```Java
{
Name = vmware-carbonblackedr-leef-process-create-success-sensor
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """process_guid""" , """ingress.event.procstart""" ]
  Fields = [
    """\Wtimestamp(":|=)({time}\d{10})""",
    """\Wtype(":"|=)({operation_type}[^"]+?)\s*("|\w+=|$)""",
    """\Wusername(":"|=)(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wcomputer_name(":"|=)({dest_host}[\w\-.]+)""",
    """\Wsensor_id(":|=)({sensor_id}\d+)""",
    """\Wmd5(":"|=)({hash_md5}[^"]+?)\s*("|\w+=|$)""",
    """\Wpath(":"|=)({path}[^"]+?)\s*("|\w+=|$)""",
    """\Wparent_path(":"|=)({parent_process_path}[^"]+?)\s*("|\w+=|$)""",
    """\Wcommand_line(":"|="?)(?:|({process_command_line}.+?))\s*("|\w+=|$)""",
    """\Wpid(":|=)({process_id}\d+)""",
    """\Wprocess_guid(":"|=)({process_guid}[^"]+?)\s*("|\w+=|$)""",
    """\Wparent_process_guid(":"|=)({parent_process_guid}[^"]+?)\s*("|\w+=|$)""",
    """\Wpath(":"|=)({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/"]+?))\s*("|\w+=|$)""",
    """\Wparent_path(":"|=)({parent_process_path}({parent_process_dir}(?:[^"]+?)?[\\\/])?({parent_process_name}[^\\\/"]+?))\s*("|\w+=|$)""",
    """\Wcommand_line(":"|="?)(\\"*)?(\w+|((([^"]+)?[\\\/])?([^\\\/"\s]+)))(?:[^\s]*)?\s*\/({arg}[^\s"]+)""",

    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.type,exa_field_name=operation_type""",
    """exa_json_path=$.username,exa_regex=^(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.computer_name,exa_regex=^({dest_host}[\w\-.]+)$""",
    """exa_json_path=$.sensor_id,exa_field_name=sensor_id""",
    """exa_json_path=$.md5,exa_field_name=hash_md5""",
    """exa_json_path=$.path,exa_field_name=path""",
    """exa_json_path=$.command_line,exa_field_name=process_command_line""",
    """exa_json_path=$.pid,exa_field_name=process_id""",
    """exa_json_path=$.process_guid,exa_field_name=process_guid""",
    """exa_json_path=$.parent_process_guid,exa_field_name=parent_process_guid""",
    """exa_json_path=$.path,exa_regex=^({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/"]+?))$""",
    """exa_json_path=$.command_line,exa_regex=(\\"*)?(\w+|((([^"]+)?[\\\/])?([^\\\/"\s]+)))(?:[^\s]*)?\s*\/({arg}[^\s"]+)"""
]
DupFields = [ "process_dir->process_path_directory"]


}
```