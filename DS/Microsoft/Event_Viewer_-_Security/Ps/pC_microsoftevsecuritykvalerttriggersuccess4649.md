#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-alert-trigger-success-4649
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """EventCode=4649""", """Message=A replay attack was detected.""", """SourceName =Microsoft Windows security auditing""", """TaskCategory=Other Logon/Logoff Events""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({host}[^\s]+)""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """Message=({event_name}[^:]+?)\s+\w+:""",
    """Subject:\s+Security ID:\s+({user_sid}[^:]+?)\s+Account Name:""",
    """Subject:.+?Account Name:\s+({user}[^\s]+)""",
    """Subject:.+?Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
    """Subject:.+?Logon ID:\s+({login_id}[^\s]+)""",
    """Process ID:\s+({process_id}[^\s]+)""",
    """Process Name:\s+({process_path}(({process_dir}[^\s]+?)\\+)?({process_name}[^\s]+))\s+Network Information:""",
    """Logon Process:\s+({auth_process}[^\s]+)""",
    """Authentication Package:\s+({auth_package}[^\s]+)""",
    """({additional_info}This event indicates that[^$]+?)\s*$"""
  ]
  DupFields = [ "event_name->alert_name", "auth_process->alert_type" ]
  ParserVersion = "v1.0.0"


}
```