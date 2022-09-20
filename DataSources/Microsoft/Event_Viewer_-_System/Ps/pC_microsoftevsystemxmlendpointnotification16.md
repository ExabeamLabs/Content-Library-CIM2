#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-notification-16
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>16</EventID>""", """<Provider Name ='Microsoft-Windows-Kernel-General'""" ]
  Fields = [
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'""",
    """<Message>\s*({additional_info}[^<]+)<\/Message>""",
    """(<EventID)?>({event_code}\d+)<\/EventID>""",
    """ProcessID='({process_id}\d+)'""",
    """Security UserID='({user_sid}[^']+)'""",
    """<Data Name ='FailureReason'>({result_code}[^<]+)<\/Data>""",
    """Data Name ='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """Data Name ='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """Data Name ='Ipaddress'>({src_ip}[^<]+)<\/Data>""",
    """Data Name ='SubjectLogonId'>({login_id}[^<]+)<\/Data>"""
  ]


}
```