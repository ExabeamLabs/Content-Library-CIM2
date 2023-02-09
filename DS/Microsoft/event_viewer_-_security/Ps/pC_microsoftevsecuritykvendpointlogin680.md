#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-680
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ "EventCode=680" ]
  Fields = [
  """({event_name}Logon attempt)""",
    """EventCode=({event_code}\w+)""",
    """Logon account:\s+({user}[^@]+?)(?:@({domain}[^\s.]+)[^\s]*)?\s+Source Workstation:\s+({dest_host}[^\s]+)""",
    """Error Code:\s+({result_code}[\w\-]+)""",
    """Sid=({user_sid}[^\s]+)\s+SidType""",
    """ComputerName =[^.\s]+(\.({domain}[^.\s]+))?"""
  ]


}
```