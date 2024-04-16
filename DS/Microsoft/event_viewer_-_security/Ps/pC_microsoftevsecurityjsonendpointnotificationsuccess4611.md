#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-success-4611
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = ["""Event ID : 4611""", """A trusted logon process has been registered"""]
    Fields = [
        """Event Time\s+:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
        """Computer : ({host}[\w\-.]+)""",
        """Event ID : ({event_code}\d+)""",
        """Security ID:\s+({user_sid}.+?)\s+Account Name:\s+(?=\w)({user}[\w\.\-]{1,40}\$?)\s+Account Domain:\s+(?=\w)({domain}.+?)\s+Logon ID""",
        """Logon ID:\s+({login_id}.+?)\s+Logon Process Name:\s+({auth_process}[^\s]+)"""
    ]
    DupFields = [ "host->dest_host" ]
  

}
```