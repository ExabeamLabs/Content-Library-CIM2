#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-logout-4647
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
  Conditions = [ """<EventID>4647</EventID>""", """<Task>Logoff""", """User initiated logoff""" ]
  Fields = [
    """({event_name}User initiated logoff)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Data Name\\*=('|")TargetUserSid('|")>({user_sid}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")TargetDomainName('|")>({domain}[^<]+)<\/Data>""",
    """<Data Name\\*=('|")TargetUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>""",
    """<Data Name\\*=('|")TargetLogonId('|")>({login_id}[^<]+)<\/Data>"""
    """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "login_id->dest_login_id" , "user_sid->dest_user_sid" , "domain->dest_domain", "user->dest_user" ]


}
```