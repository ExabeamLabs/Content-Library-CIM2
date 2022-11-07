#### Parser Content
```Java
{
Name = microsoft-evsystem-xml-dcom-activate-fail-10016
  ParserVersion = v1.0.0 
  Conditions = [ """>10016</EventID>""", """This security permission can be modified using the Component Services administrative tool.""" ]

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