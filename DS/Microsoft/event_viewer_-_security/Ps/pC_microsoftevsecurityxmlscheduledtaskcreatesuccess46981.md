#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4698-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4698</EventID>""",
"""TaskName""",
"""<Data Name"""
]
Fields = [
"""SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
 """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<EventID>({event_code}[^<]+)</EventID>"""
"""<Data Name(\\)?=('|")SubjectUserSid('|")>(?:NONE_MAPPED|({user_sid}[^<]+))</Data>"""
"""<Data Name(\\)?=('|")SubjectUserName('|")>(?=\w)({user}[\w\.\-]{1,40}\$?)</Data>"""
"""<Data Name(\\)?=('|")SubjectDomainName('|")>(?=\w)({domain}[^<]+)</Data>"""
"""<Data Name(\\)?=('|")SubjectLogonId('|")>(?=\w)({login_id}[^<]+)</Data>"""
"""<Data Name(\\)?=('|")TaskName('|")>(?=[\\\w])({task_name}[^<]+)</Data>"""
"""<UserId>(?=\w)(({account_domain}[^\\<]*)\\)?({account_name}[^<]+)</UserId>"""
"""<Settings>\s*({additional_info}.+?)\s*</Settings>"""
"""<Triggers>\s*({triggers}.+?)\s*</Triggers>"""
"""<RunLevel>(?=\w)({run_level}[^<]+)</RunLevel>"""
"""<LogonType>(?=\w)({login_type_text}[^<]+)</LogonType>"""
"""<RegistrationInfo>.+?<Author>(?=\w)({author}[^<]+)</Author>"""
"""<RegistrationInfo>.+?<Description>(?=\w)({description}[^<]+)</Description>"""
"""<Command>\"?({process_path}({process_dir}(?:(\w+:)?[^:<\"]+)?[\\\/])?({process_name}[^<\"]+))"""
"""<Arguments>(\"+)?({arg}[^<\"]+)"""
"""<Message>({event_name}A scheduled task was created)"""
]
ParserVersion = "v1.0.0"


}
```