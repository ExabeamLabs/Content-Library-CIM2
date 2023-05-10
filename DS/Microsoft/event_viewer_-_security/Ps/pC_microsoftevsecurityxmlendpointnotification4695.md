#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4695
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>4695</EventID>""", """Unprotection of auditable protected data was attempted.""" ]
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
    """Data Name ='Ipaddress'>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data>""",
    """Data Name ='SubjectLogonId'>({login_id}[^<]+)<\/Data>"""
    """({event_name}Unprotection of auditable protected data was attempted)"""
  ]


}
```