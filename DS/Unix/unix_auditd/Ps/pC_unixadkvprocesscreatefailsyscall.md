#### Parser Content
```Java
{
Name = unix-ad-kv-process-create-fail-syscall
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS","MMM dd HH:mm:ss","epoch_sec"]
  Conditions = [
"""SYSCALL""",
"""success=no""",
""" msg=""",
""" ppid=""",
"""audit"""
  ]
  Fields = [
    """msg=audit\(({time}\d{10}).\d+:\d+""",
    """({time}\w+\s\d+\s\d+:\d+:\d+)?\s*({host}[\w\-.]+)\s*audispd:""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """exe=\"({process_path}[^\"]*)\"""",
    """exe=\"({process_dir}.+\/)({process_name}.+?)\"""",
    """\d\d:\d\d\s+({host}({dest_host}[\w\-.]+))\s+""",
    """\sppid=({parent_process_id}.+?)\s+(\w+=|$)""",
    """\spid=({process_id}.+?)\s+(\w+=|$)""",
    """\suid=({user_id}.+?)\s+(\w+=|$)""",
    """\sgid=({group_id}.+?)\s+(\w+=|$)""",
    """\sauid=({account_id}.+?)\s+(\w+=|$)""",
    """\sses=({session_id}\d+)\s+(\w+=|$)""",
    """\stype=({operation_type}.+?)\s+(\w+=|$)""",
    """\skey="({failure_reason}[^"]+)""""
    """node=({dest_host}[\w\-.]+)"""
    """\sUID="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """SYSCALL=({syscall_name}[^"\s]+)"""
    """syscall=({syscall_number}\d+)"""
    """comm="({process_command_line}[^"\\]+)"""
    """arch=({system_architecture}[^"\s]+)"""
  ]


}
```