#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-member-remove-success-4762
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """4762""", """(EventID 4762)""" , """A member was removed from a security-disabled universal group""" , """Microsoft Windows security auditing""" ]
  Fields = ${DLWindowsParsersTemplates.windows-group-membership-events.Fields}[
    """({event_name}A member was removed from a security-disabled universal group)""",
  ]

windows-group-membership-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+MSWinEventLog""",
    """Logon ID:\s+({login_id}[^\s]+)\s+""",
    """Security ID:\s+({user_sid}[^:]+?)\s+Account Name:""",
    """Account Name:\s+(LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s+(NT AUTHORITY|({domain}[^\s]+))\s+Logon ID:""",
    """Group:\s+(|-|({group_name}[^:]+?))\s+Security ID:\s+(|-|({group_id}[^:]+?))\s+Group Name:\s+(|-|({=group_name}[^:]+?))\s+Group Domain:\s+(|-|({group_domain}[^\s]+))\s""",
    """Changed Attributes:\s+(|-|([^:]+?))\s+SAM Account Name:\s+(|-|([^:]+?))\s+SID History:\s+(|-|({sid_history}[^:]+?))\s+Additional Information:""",
# DL Fields are removed
    """Additional Information:\s+(|-|({additional_info}[^:]+?))\s+Privileges:\s+(|-|({privileges}[^:]+?))\s+(\(|$)"""
 
}
```