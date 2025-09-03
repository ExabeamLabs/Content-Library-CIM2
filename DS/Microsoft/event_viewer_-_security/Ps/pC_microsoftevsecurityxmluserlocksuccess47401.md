#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-user-lock-success-4740-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""<EventID>4740</EventID>"""
"""A user account was locked out"""
]
Fields = [
"""({event_name}A user account was locked out)"""
"""SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""<Computer>({host}[\w\-.]+)</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
"""<EventID>({event_code}[^<]+)</EventID>"""
"""Subject:[^=]+?Account Name:\s*([\\t]*)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was"""
"""Account That Was Locked Out:\s*([\\t]*)Security ID:\s*([\\t]*)({user_sid}[^:]+?)\s*([\\t]*)Account Name:\s*([\\t]*)({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Additional"""
"""Caller Computer Name:\s*([\\t]*)(?:\\+)?({src_host}[^<=\s]+)(<|\s)"""
"""<Data Name\\*=('|")TargetUserName('|")>({account}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
"""<Data Name\\*=('|")TargetSid('|")>({user_sid}[^<]+)<"""
"""<Data Name\\*=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<"""
"""<Data Name\\*=('|")SubjectDomainName('|")>({domain}[^<]+)<"""
"""<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)<"""
"""<Data Name\\*=('|")TargetDomainName('|")>(?:\\+)?({src_host}[^<=\s]+)(<|\s)"""
"""<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```