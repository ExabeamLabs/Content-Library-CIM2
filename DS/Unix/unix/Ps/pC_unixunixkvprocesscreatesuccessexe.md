#### Parser Content
```Java
{
Name = unix-unix-kv-process-create-success-exe
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["epoch_sec","MM/dd/yyyy HH:mm:ss.SSS"]
  Conditions = [
"""SYSCALL""",
""" uid=""",
"""syscall=""",
""" exe="""
  ]
  Fields = [
    """\suid=({user_id}.+?)\s+(\w+=|$)""",
    """\stype=({operation_type}.+?)\s+(\w+=|$)""",
    """\w+\s*\d{1,2} \d\d:\d\d:\d\d\s+({host}[\w\-.]+)""",
    """({host}[\w\-.]+)\s*(vcsa-audit|audispd:)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w\-.]+)""",
    """msg=audit\(({time}(\d{10})|\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\.\d+)""",
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
    """node=({dest_host}[\w\-.]+)"""
    """type=({operation_type}\S+)"""
    """exit=(\d|({failure_code}[^\(=]+?)\(({failure_reason}[^=]+?))\)\s+\w+="""
    """\sUID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """SYSCALL=({syscall_name}[^"\s]+)"""
    """syscall=({syscall_number}\d+)"""
    """comm="({process_command_line}[^"\\]+)"""
    """arch=({system_architecture}[^"\s]+)"""
  ]


}
```