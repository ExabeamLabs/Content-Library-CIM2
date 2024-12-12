#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-scheduled-task-create-success-106
  Vendor = "Microsoft"
  Product = "Event Viewer - TaskScheduler"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [ """<EventID>106<""", """Microsoft-Windows-TaskScheduler""", """TaskRegisteredEvent""" ]
  Fields = [
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7,9}Z)('|")""",
    """<Computer>({host}({dest_host}[\w\-\.]+))<""",
    """<Security UserID=('|")({user_sid}[^'"<]+?)('|")""",
    """<Data Name =(('|")TaskName('|")>({task_name}[^<]+))""",
    """<Data Name =('|")UserContext('|")>(((?i)NT AUTHORITY\\System)|(({domain}[^\\\/<]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """({event_code}106)""",
    """({event_name}Task registered)""",
    """<Message>({additional_info}[^<]+)<""",
    """<Level>({run_level}[^<]+)<"""
    """ProcessID(\\)?=('|")({process_id}[^'"]+)"""
    """ThreadID(\\)?=('|")({thread_id}[^'"]+)"""
    """EventData Name(\\)?=('|")({event_name}[^'"\>]+)"""
    """<Channel>({channel}[^<]+)<"""
    """<Keywords>({result}[^<]+)</Keywords>"""
    """Provider Name\\*=('|")({provider_name}[^\'"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```