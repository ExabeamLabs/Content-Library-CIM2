#### Parser Content
```Java
{
Name = "microsoft-windows-xml-log-clear-success-104"
Vendor = "Microsoft"
Product = "Event Viewer - System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [ """<EventID>104<""", """<Provider Name =""" ]
Fields = [
"""<EventID>({event_code}\d+)"""
"""<Keywords>({result}[^<]+)"""
"""<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""<Computer>({host}[\w\-.]+)"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<Computer>(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))"""
"""<Security UserID\\*='({user_sid}[^'<\/]+)"""
"""<SubjectUserName>(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""<SubjectDomainName>(NT AUTHORITY|({domain}[^<]+))"""
"""<Message>({event_name}[^<]+)"""
"""<Level>({run_level}[^<]+)"""
]
DupFields = ["user->src_user" , "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```