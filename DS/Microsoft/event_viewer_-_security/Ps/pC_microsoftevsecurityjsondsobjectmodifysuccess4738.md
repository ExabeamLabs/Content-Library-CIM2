#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-modify-success-4738"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID"""
""":4738"""
"""A user account was changed"""
]
Fields = [
"""({event_name}A user account was changed)"""
"""({event_code}4738)"""
""""TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
""""EventTime\\?":\s*\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\\?""""
""""Host(N|n)ame\\?":\\?"({host}[^"]+)""""
""""(hostname|Computer)":"({host}[^"]+)""""
""""SeverityValue\\?":\\?"({severity}[^,]+)""""
""""TargetUserName\\?":\\?"({dest_user}[^"\\]+)"""
""""TargetDomainName\\?":\\?"({dest_domain}[^"\\]+)"""
""""TargetSid\\?":\\?"({dest_user_sid}[^"\\]+)"""
""""SubjectUserSid\\?":\\?"({user_sid}[^"\\]+)"""
""""SubjectUserName\\?":\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""SubjectDomainName\\?":\\?"({domain}[^"\\]+)"""
""""SubjectLogonId\\?":\\?"({login_id}[^"\\]+)"""
""""+Category\\?"+:\\?"+({category}[^"\\]+)"""
""""+Message\\?"+:\\?"+({additional_info}[^"\\]+)"""
""""+EventType\\?"+:\\?"+({result}[^"\\]+)"""
]
DupFields = [ "event_name->additional_info", "user->src_user", "domain->src_domain"]
ParserVersion = "v1.0.0"


}
```