#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-4797
  Vendor = Microsoft
  Product = Event Viewer - System
  Conditions = [ """Microsoft Windows security auditing""", """EventCode=4797""", """An attempt was made to query the existence of a blank password for an account""" ]
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Fields = [
    """ComputerName =({host}[^\s]+)""",
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(am|AM|pm|PM))""",
    """({event_code}4797)""",
    """({event_name}An attempt was made to query the existence of a blank password for an account)""",
    """Account Name:\s*({user}[^\s:]+)""",
    """Account Domain:\s*({domain}[^\s:]+)""",
    """Logon ID:\s*({login_id}[^\s:]+)""",   
    """Additional Information:\s*({additional_info}.+?)$"""
    """RecordNumber=({event_id}\w+)"""
    """LogName =({log_name}[^\s]+)"""
    """Security ID:\s*({user_sid}\S+)\s+Account Name:"""
  ]
  ParserVersion = v1.0.0


}
```