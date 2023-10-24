#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-endpoint-password-modify-5823
  ParserVersion = v1.0.0
  Conditions = [ """>5823</EventID>""", """The system successfully changed its password on the domain controller""" ]

windows-events-5 = {
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'""",
    """<Message>\s*({additional_info}[^<]+)<\/Message>""",
    """(<EventID)?>({event_code}\d+)<\/EventID>""",
    """ProcessID\\*='({process_id}\d+)'""",
    """Security UserID\\*='({user_id}[^']+)'""",
    """<Data Name\\*='FailureReason'>({result_code}[^<]+)<\/Data>""",
    """Data Name\\*='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """Data Name\\*='SubjectUserName'>({user}[\w\.\-]{1,40}\$?)<\/Data>""",
    """Data Name\\*='Ipaddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data>""",
    """Data Name\\*='SubjectLogonId'>({login_id}[^<]+)<\/Data>""",
    """\WCLSID\s*\{({cls_id}[^}\s]+)\}\s*"""
    
  
}
```