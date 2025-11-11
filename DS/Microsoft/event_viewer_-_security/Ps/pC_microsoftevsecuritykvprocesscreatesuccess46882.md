#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-process-create-success-4688-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyyMMddHHmmss"
  Conditions = [ """"EventCode = 4688;"""", """A new process has been created""" ]
  Fields = [
    """({event_name}A new process has been created)""",
    """Computer(Name)? = "+({src_host}({host}[\w\-.]+))"""",
    """EventCode = ({event_code}\d+)""",
    """TimeGenerated = "({time}[\d]+)\.\d\d\d""",
    """Account Name:\s+(?:|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s+(?:|({domain}.+?))\s+Logon ID:""",
    """New Process Name:\s+(?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Token Elevation Type:""",
    """New Process Name:\s+(?:|({path}.+?))\s+Token Elevation Type:"""
    """Logon ID:\s+({login_id}[^\s]+)\s+Process""",
    """Security ID:\s+({user_sid}[^\s]+)\s""",
    """Process Command Line:\s+(?:|({process_command_line}.+?))\s+Token Elevation Type """,
    """Process Command Line:\s*(|-|(sc|((?:[^"]+)?[\\\/])?sc.exe)\s*(?:\\*[\w.\-]+)?\s*create\s*({service_name}.+?))\s+binPath= (?:|({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/\s]+)))\s+Token Elevation Type """,
    """Creator Process ID:\s+({parent_process_guid}[^\s]+)\s""",
    """New Process ID:\s+({process_id}({process_guid}[^\s]+))\s""",
    """({operation_type}Process Creation)"""
  ]


}
```