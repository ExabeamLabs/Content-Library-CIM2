#### Parser Content
```Java
{
Name = unix-unix-kv-process-create-success-exe
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "epoch_sec"
  Conditions = [
"""type=SYSCALL""",
""" uid=""",
"""syscall=""",
""" exe="""
  ]
  Fields = [
    """\suid=({user_id}.+?)\s+(\w+=|$)""",
    """\stype=({operation_type}.+?)\s+(\w+=|$)""",
    """\w+\s*\d{1,2} \d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """({host}[\w.\-]+)\s+audispd:""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w\-.]+)""",
    """msg=audit\(({time}\d{10})""",
    """\sppid=({parent_process_id}[^=]+?)\s+(\w+=|$)""",
    """\sexe=\\?"({process_command_line}[^"\\]+)\\?"""",
    """\sexe=\\?"({process_path}(({process_dir}[^\"]*?/+))?({process_name}[^"\\\/]+))\\?"""",
    """\spid=({process_id}[^=]+?)\s+(\w+=|$)""",
    """\sgid=({group_id}[^=]+?)\s+(\w+=|$)""",
    """\sauid=({account_id}[^=]+?)\s+(\w+=|$)""",
    """\skey=\\?"({object}[^\"]+)\\?"""",   
    """\smsg=audit\(({command_id}\d+\.\d+)""",
    """\ssuccess=(|({result}.+?))(\s+\w+=|\s*$)""",
    """\skey=({additional_info}[^\s"\\]+)"""    
  ]
  DupFields = [ "host->src_host" ]


}
```