#### Parser Content
```Java
{
Name = unix-ad-kv-endpoint-notification-permissioncheck
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "epoch_sec"
  Conditions = [ """Auditd: SELinux permission check""", """type=AVC""", """ denied """ ]
  Fields = [
    """"description":"({description}[^"]+)""",
    """"groups":\[({groups}[^\]]+?)\]""",
# euid is removed
    """"command":"({process_name}[^"]+)""",
    """"location":"({log_location}[^"]+)""",
    """"path":"({log_path}[^"]+)""",
    """"agent":\{[^\}]*?"name":"({agent_name}[^"]+)""",
    """type=({event_category}AVC)""",
    """msg=audit\(({time}\d{10})""",
    """\savc:\s*({access}denied)\s*\{\s*({permission}[^\}]+?)\s*\}""",
    """for pid=({process_id}\d+)""",
    """\sexe=\\"({process_path}({process_dir}[^"]+?)\/[^"\\\/]+)\\""""
    """\scomm=\\"({process_name}[^\\"]+)\\"""",
# target_name is removed
# inode_number is removed
# src_context is removed
# target_context is removed
    """\stclass=({file_type}[^=]+?)(\s+\w+=|\s*$)""",
    """\suid=({user_id}\d+)""",
    """\sgid=({group_id}\d+)""",
  ]
  DupFields = [ "target_name->file_name" ]


}
```