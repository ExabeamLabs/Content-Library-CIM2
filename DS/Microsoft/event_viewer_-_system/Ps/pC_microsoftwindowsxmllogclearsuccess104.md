#### Parser Content
```Java
{
Name = "microsoft-windows-xml-log-clear-success-104"
Vendor = "Microsoft"
Product = "Event Viewer - System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [ """<EventID>104<""", """log file was cleared.""" ]
Fields = [
"""<EventID>({event_code}\d+)"""
"""<Keywords>({result}[^<]+)"""
"""<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""<Computer>({host}[\w\-.]+)"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<Computer>(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))"""
"""<Security UserID\\*='({user_sid}[^'<\/]+)"""
"""<SubjectUserName>(SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
"""<SubjectDomainName>(NT AUTHORITY|({domain}[^<]+))"""
"""<Message>({event_name}[^<]+)"""
"""<Level>({alert_severity}[^<]+)"""
]
ParserVersion = "v1.0.0"
DupFields = [ "host->src_host" ]


}
```