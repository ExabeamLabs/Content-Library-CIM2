#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-success-5380
   Product = Event Viewer - Security
   Vendor = Microsoft
   ParserVersion = v1.0.0
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
   Conditions = [ """<EventID>5380<""", """Microsoft-Windows-Security-Auditing""" ]
   Fields =[
      """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
      """<Computer>({host}({dest_host}[\w\-\.]+))</Computer>""",
      """<Data Name\\*=('|")SubjectUserSid('|")>(-|({user_sid}[^<>]+))<""",
      """<Data Name\\*=('|")SubjectUserName('|")>(-|({user}[\w\.\-]{1,40}\$?))<""",
      """<Data Name\\*=('|")SubjectDomainName('|")>(-|({domain}[^<>]+))<""",
      """<Data Name\\*=('|")SubjectLogonId('|")>(-|({login_id}[^<>]+))<"""
      """<Level>({run_level}[^<]+)<"""
     ]
   

}
```