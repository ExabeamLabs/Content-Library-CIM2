#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-list-4799
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  ParserVersion = "v1.0.0"
  Conditions = [ """4799""", """A security-enabled local group membership was enumerated""" ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """({event_code}4799)""",
    """(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(am|pm|({host}[\w\-.]+))""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s""",
    """({event_name}A security-enabled local group membership was enumerated)""",
    """Subject:\s*[^"]+?Security ID:\s*({user_sid}[^\s]+)\s+Account Name:""",
    """Subject:\s*[^"]+?Account Name:\s*(-|({user}[^\s]+))""",
    """Subject:\s*[^"]+?Account Domain:\s*(-|({domain}[^\s]+))""",
    """Subject:\s*[^"]+?Logon ID:\s*({login_id}[^\s]+)""",
    """Group:\s*[^"]+?Security ID:\s+({group_id}[^\s]+)""",
    """Group:\s*[^"]+?(Group|Account) Name:\s+({group_name}.+?)?\s+(Group|Account) Domain:""",
    """Group:\s*[^"]+?(Group|Account) Domain:\s+({group_domain}[^\s]+)""",
    """Process ID:\s*[^"]+?\s+({process_id}[^\s]+)""",
    """Process Name:\s+({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))(\s|<|")""",
  ]


}
```