#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-logout-4634
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4634</EventID>""", """<TimeCreated SystemTime=""", """<Data Name =""" ]
  Fields = [
    """<Message>({event_name}[^.。]+)""",
    """({event_name}An account was logged off)""",
    """<TimeCreated SystemTime=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z('|")\/>""",
    """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """<Data Name =('|")LogonType('|")>({login_type}\d+)<\/Data>""",
    """<Data Name =('|")TargetUserSid('|")>({user_sid}[^<]+)<\/Data>""",
    """<Data Name =('|")TargetDomainName('|")>((?i)NT AUTHORITY|({domain}[^<]+))<\/Data>""",
    """<Data Name =('|")TargetUserName('|")>((?i)SYSTEM|({user}[^<]+))<\/Data>""",
    """<Data Name =('|")TargetLogonId('|")>({login_id}[^<]+)<\/Data>"""
  ]


}
```