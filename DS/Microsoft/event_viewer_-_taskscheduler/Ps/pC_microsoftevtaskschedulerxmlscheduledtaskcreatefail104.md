#### Parser Content
```Java
{
Name = "microsoft-evtaskscheduler-xml-scheduled-task-create-fail-104"
Vendor = "Microsoft"
Product = "Event Viewer - TaskScheduler"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [ """<EventID>104<""", """<Provider Name =""", """<Channel>Microsoft-Windows-TaskScheduler""" ]
Fields = [
"""<EventID>({event_code}\d+)"""
"""<Keywords>({result}[^<]+)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""<Computer>({src_host}({host}[\w\-.]+))"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))""",
"""<Computer>(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))"""
"""<Security UserID\\*=('|")({user_sid}[^'<\/"]+)"""
"""<SubjectUserName>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
"""<SubjectDomainName>(NT AUTHORITY|({src_domain}({domain}[^<]+)))"""
"""<Level>({alert_severity}[^<]+)"""
"""ProcessID=('|")({process_id}[^\s']+)"""
"""ThreadID=('|")({thread_id}[^']+)"""
"""<Channel>({channel}[^<]+)<"""
"""<EventData Name ='({event_name}[^>']+)"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```