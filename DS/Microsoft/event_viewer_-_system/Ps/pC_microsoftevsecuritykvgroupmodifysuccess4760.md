#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-modify-success-4760
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """(EventID 4760)""", """A security-disabled universal group was changed""" , """Microsoft Windows security auditing""" ]
  Fields = ${DLWindowsParsersTemplates.windows-group-membership-events.Fields}[
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+MSWinEventLog""",
    """({event_name}A security-disabled universal group was changed)""",
  ]

windows-group-membership-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """Logon ID:\s+({login_id}[^\s]+)\s+""",
    """Security ID:\s+({user_sid}S-\d+-[^:]+?)\s+Account Name:""",
    """Account Name:\s+(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s+(NT AUTHORITY|({domain}[^\s]+))\s+Logon ID:""",
    """Group:\s+(|-|({group_name}[^:]+?))\s+Security ID:\s+(|-|({group_id}[^:]+?))\s+Group Name:\s+(|-|({=group_name}[^:]+?))\s+Group Domain:\s+(|-|({group_domain}[^\s]+))\s""",
    """Changed Attributes:\s+(|-|([^:]+?))\s+SAM Account Name:\s+(|-|([^:]+?))\s+SID History:\s+(|-|({sid_history}[^:]+?))\s+Additional Information:""",
# DL Fields are removed
    """Additional Information:\s+(|-|({additional_info}[^:]+?))\s+Privileges:\s+(|-|({privileges}[^:]+?))\s+(\(|$)"""
 
}
```