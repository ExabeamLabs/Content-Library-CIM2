#### Parser Content
```Java
{
Name = vmware-carbonblackedr-leef-process-create-success-sensor
    ParserVersion = v1.0.0
    Vendor = VMware
    Product = Carbon Black EDR
    TimeFormat = "epoch_sec"
   Conditions = [ """process_guid""" , """ingress.event.procstart""" ]
  Fields = [
    """\Wtimestamp(":|=)({time}\d{10})""",
    """\Wtype(":"|=)({operation_type}[^"]+?)\s*("|\w+=|$)""",
    """\Wusername(":"|=)(({domain}[^\\]+)\\+)?({user}[^"\s]+)""",
    """\Wcomputer_name(":"|=)({dest_host}[\w\-.]+)""",
    """\Wsensor_id(":|=)({sensor_id}\d+)""",
    """\Wmd5(":"|=)({hash_md5}[^"]+?)\s*("|\w+=|$)""",
    """\Wpath(":"|=)({path}[^"]+?)\s*("|\w+=|$)""",
    """\Wparent_path(":"|=)({parent_process}[^"]+?)\s*("|\w+=|$)""",
    """\Wcommand_line(":"|="?)(?:|({process_command_line}.+?))\s*("|\w+=|$)""",
    """\Wpid(":|=)({process_id}\d+)""",
    """\Wprocess_guid(":"|=)({process_guid}[^"]+?)\s*("|\w+=|$)""",
    """\Wparent_process_guid(":"|=)({parent_process_guid}[^"]+?)\s*("|\w+=|$)""",
    """\Wpath(":"|=)({process_path}({process_dir}(?:[^"]+?)?[\\\/])?({process_name}[^\\\/"]+?))\s*("|\w+=|$)""",
    """\Wparent_path(":"|=)({parent_process}({parent_process_dir}(?:[^"]+?)?[\\\/])?({parent_process_name}[^\\\/"]+?))\s*("|\w+=|$)""",
    """\Wcommand_line(":"|="?)(\\"*)?(\w+|((([^"]+)?[\\\/])?([^\\\/"\s]+)))(?:[^\s]*)?\s*\/({arg}[^\s"]+)"""
]
DupFields = [ "process_dir->process_path_directory"]


}
```