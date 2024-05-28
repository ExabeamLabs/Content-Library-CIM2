#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-service-create-success-4697"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ" ]
Conditions = [
"""<EventID>4697</EventID>"""
"""ServiceFileName"""
"""<Data Name"""
]
Fields = [
"""SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<EventID>({event_code}[^<]+)</EventID>"""
"""<Data Name(\\)?=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name(\\)?=('|")SubjectUserName('|")>(?=\w)({user}[\w\.\-]{1,40}\$?)</Data>"""
"""<Data Name(\\)?=('|")SubjectDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
"""<Data Name(\\)?=('|")SubjectLogonId('|")>(?=\w)({login_id}[^<]+)</Data>"""
"""<Data Name(\\)?=('|")ServiceName('|")>(?=\w)(({service_name}[^_]+?)(_[^\<]+)?)</Data>"""
"""<Data Name(\\)?=('|")ServiceAccount('|")>(?=\w)(({account_domain}[^\\<]*)\\)?({account_name}[^<]+)</Data>"""
"""<Data Name(\\)?=('|")ServiceFileName('|")>\"?(?=\w)({process_path}({process_dir}(?:(\w+:)?[^:<\"]+)?[\\])?({process_name}[^<\"\s]+))"""
"""<Data Name(\\)?=('|")ServiceType('|")>(?=\w)({service_type}[^<]+)</Data>"""
"""<Message>({event_name}A service was installed in the system)"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```