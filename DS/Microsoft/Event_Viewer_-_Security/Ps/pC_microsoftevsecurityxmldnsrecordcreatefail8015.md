#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-dns-record-create-fail-8015
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>8015</EventID>""", """Data Name ='AdapterSuffixName'""" ]

windows-events-5 = {
  Vendor = Microsoft
  Product = Event Viewer - System
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[^<]+)<\/Computer>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)'""",
    """<Message>\s*({additional_info}[^<]+)<\/Message>""",
    """(<EventID)?>({event_code}\d+)<\/EventID>""",
    """ProcessID='({process_id}\d+)'""",
    """Security UserID='({user_id}[^']+)'""",
    """<Data Name ='FailureReason'>({result_code}[^<]+)<\/Data>""",
    """Data Name ='SubjectDomainName'>({domain}[^<]+)<\/Data>""",
    """Data Name ='SubjectUserName'>({user}[^<]+)<\/Data>""",
    """Data Name ='Ipaddress'>({src_ip}[^<]+)<\/Data>""",
    """Data Name ='SubjectLogonId'>({login_id}[^<]+)<\/Data>""",
    """\WCLSID\s*\{({cls_id}[^}\s]+)\}\s*"""
    
  
}
```