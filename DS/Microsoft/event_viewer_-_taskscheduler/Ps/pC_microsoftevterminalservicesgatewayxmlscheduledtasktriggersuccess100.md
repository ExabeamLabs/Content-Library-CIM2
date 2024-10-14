#### Parser Content
```Java
{
Name = microsoft-evterminalservicesgateway-xml-scheduled-task-trigger-success-100
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - TaskScheduler
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>100</EventID>""", """<Provider Name =""","""<Channel>Microsoft-Windows-TaskScheduler/Operational</Channel>""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<Computer>({host}[\w\-\.]+)<""",
    """<Security UserID=('|")({user_sid}[^'"<]+?)('|")""",
    """<Data Name =(('|")TaskName('|")>({task_name}[^<]+))""",
    """<Data Name =('|")UserContext('|")>(((?i)NT AUTHORITY\\System)|(({domain}[^\\\/<]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """({event_code}100)""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```