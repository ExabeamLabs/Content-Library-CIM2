#### Parser Content
```Java
{
Name = microsoft-windows-kv-policy-modify-success-4947
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = ["""EventCode=4947""", """Microsoft Windows security auditing""", """A change was made to the Windows Firewall exception list"""]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(am|AM|pm|PM))""",
    """EventCode=({event_code}\d+)\s*""",
    """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)\s+""",
    """({event_name}A change was made to the Windows Firewall exception list)""",
    """ComputerName =({host}[\w.\-]+)"""
    """RecordNumber=({event_id}\w+)"""
    """LogName =({log_name}[^\s]+)"""
    """Rule Name:\s*({rule}[^:]+)""",
    """Rule ID:\s*({rule_id}[^\s]+)\s""",
    """Keywords=({result}[^=]+)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```