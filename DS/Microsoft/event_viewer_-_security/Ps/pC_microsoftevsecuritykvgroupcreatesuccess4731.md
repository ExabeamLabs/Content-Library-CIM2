#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-create-success-4731
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """A security-enabled local group was created""", """4731""", """Microsoft-Windows-Security-Auditing""", """Subject:""" ]
  Fields = [
    """({event_name}A security-enabled local group was created)""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d{4})\s+({event_code}4731)\s+Microsoft-Windows-Security-Auditing""",
    """({result}(Success|Failure) Audit)\s+({host}[\w\-\.]+)\s+Security Group Management""",
    """Subject:\s+Security ID:\s*({user_sid}[^:]+?)\s+Account Name:""",
    """Subject:[^"]+?Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:""",
    """Subject:[^"]+?Account Domain:\s*({domain}[^:]+?)\s+Logon ID:""",
    """Subject:[^"]+?Logon ID:\s*({login_id}[^:]+?)\s+New Group:""",
    """New Group:\s+Security ID:\s*({group_id}[^:]+?)\s+Group Name:""",
    """New Group:[^"]+?Group Name:\s*({group_name}[^:]+?)\s+Group Domain:""",
    """New Group:[^"]+?Group Domain:\s*({group_domain}[^:]+?)\s+Attributes:""",
    """Privileges:\s*(?:-|({privileges}[^"]+?))\s+\d+$"""
  ]
  DupFields = [ "host-> dest_host" ]
  ParserVersion = "v1.0.0"


}
```