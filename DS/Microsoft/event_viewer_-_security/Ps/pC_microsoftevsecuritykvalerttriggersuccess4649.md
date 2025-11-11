#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-alert-trigger-success-4649
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """EventCode=4649""", """Message=A replay attack was detected.""", """SourceName =Microsoft Windows security auditing""", """TaskCategory=Other Logon/Logoff Events""" ]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
    """EventCode=({event_code}\d+)""",
    """ComputerName =({host}[^\s]+)""",
    """Keywords=({result}[^=]+?)\s+\w+=""",
    """Message=({alert_name}({event_name}[^:]+?))\s+\w+:""",
    """Subject:\s+Security ID:\s+({user_sid}[^:]+?)\s+Account Name:""",
    """Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Subject:.+?Account Domain:\s+({domain}[^:]+?)\s+Logon ID:""",
    """Subject:.+?Logon ID:\s+({login_id}[^\s]+)""",
    """Process ID:\s+({process_id}[^\s]+)""",
    """Process Name:\s+({process_path}(({process_dir}[^\s]+)\\+)?({process_name}[^\s]+))\s+Network Information:""",
    """Logon Process:\s+({alert_type}({auth_process}[^\s]+))""",
    """Authentication Package:\s+({auth_package}[^\s]+)""",
    """({additional_info}This event indicates that[^$]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```