#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-permission-modify-4718
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """<EventID>4718</EventID>""", """<Event xmln""", """Correlation ActivityID""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<]+)</Computer>""",
    """<Data Name[^<>]+?AccessRemoved[^<>]+?>({access_type}[^<>]+?)</Data>""",
    """<EventID>({event_code}\d+)""",
    """<Keywords>({result}[^<]+)""",
    """<Data Name ='SubjectUserName'>({user}[^<]+)</Data>""",
    """<Data Name ='SubjectDomainName'>({domain}[^<]+)</Data>""",
    """<Data Name ='SubjectUserSid'>({user_sid}[^<]+)""",
    """<Data Name ='SubjectLogonId'>({login_id}[^<]+)</Data>""",
    """<Data Name ='AccessRemoved'>({access_removed_right}[^<]+)<""",
    """<Execution ProcessID='({process_id}\d+)""",
    """<Task>({sub_category}[^<]+)"""
  ]


}
```