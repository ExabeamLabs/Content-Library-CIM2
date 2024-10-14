#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-authentication-fail-5168
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>5168<""", """Microsoft-Windows-Security-Auditing""", """<Computer>""" ]
  Fields =[
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
    """<Data Name\\*=('|")SubjectUserSid('|")>(-|({user_sid}[^<>]+))<""",
    """<Data Name\\*=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """<Data Name\\*=('|")SubjectDomainName('|")>(-|({domain}[^<>]+))<""",
    """<Data Name\\*=('|")SubjectLogonId('|")>(-|({login_id}[^<>]+))<"""
    """<Data Name\\*=('|")ServerNames('|")>({src_host}[\w\-\.]+)""",
    """<Data Name =('|")IpAddresses('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```