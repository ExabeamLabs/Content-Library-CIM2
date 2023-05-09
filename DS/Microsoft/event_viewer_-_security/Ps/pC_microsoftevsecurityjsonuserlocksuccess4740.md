#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-lock-success-4740
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":"""
"""4740"""
"""A user account was locked out"""
]
Fields = [
"""({event_name}A user account was locked out)"""
""""EventTime\\?":\s*\\?"({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})\""""
""""Hostname\\?":\\?"({host}[\w\-.]+)"""
""""ComputerName\\?":\\?"({host}[\w\-\.]+)"""
"""({event_code}4740)"""
"""Security ID:\s*(\\t|\\r|\\n)*({user_sid}[^\s\\"]+)\s*(\\t|\\r|\\n)*Account Name:\s*(\\t|\\r|\\n)*({src_user}[^\s\\"]+)\s*(\\t|\\r|\\n)*Account Domain:\s*(\\t|\\r|\\n)*({src_domain}[^\s\\"]+)\s*(\\t|\\r|\\n)*Logon ID:\s*(\\t|\\r|\\n)*({login_id}[^\s"\\]+)\s*(\\t|\\r|\\n)*"""
""""SubjectUserName\\?":\\?"({src_user}[^\\"]+)"""
""""SubjectDomainName\":\"({src_domain}[^\\"]+)"""
""""SubjectLogonId\\?":\\?"({login_id}[^\\"]+)"""
""""TargetSid\\?":\\?"({user_sid}[^\\"]+)"""
""""TargetUserName\\?":\\?"({user}[^\\"]+)"""
"""Additional Information:(\\r|\\t|\\n)*Caller Computer Name:(\\r|\\t|\\n)*({src_host}[^\\"]+)"""
]
DupFields = [
"host->dest_host"
"src_domain->domain"
]
ParserVersion = "v1.0.0"


}
```