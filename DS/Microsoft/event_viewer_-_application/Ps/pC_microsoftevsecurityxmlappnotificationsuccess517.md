#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-notification-success-517
  Vendor = Microsoft
  Product = Event Viewer - Application
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """<EventID>517</EventID>""", """<Provider Name =""", """Microsoft-Windows-Backup""" , """<Channel>Application</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<EventID>({event_code}\d+)</EventID>""",
    """<Keywords>({result}[^\<]+)</Keywords>""",
    """<EventRecordID>({event_id}[^\<]+)</EventRecordID>""",
    """<Computer>({host}[^\<]+)</Computer>""",
    """<Message>({additional_info}[^<]+)""",
    """<Provider>({provider_name}[^<]+)""",
    """<System>.*?Guid(\\)?=('|")\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}\d+)""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """({event_name}Backup failed)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```