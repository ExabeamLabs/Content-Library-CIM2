#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-logout-4634-tl"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<eventid>4634<"""
"""an account was logged off"""
"""<data name\="""
"""targetusername"""
]
Fields = [
"""(?i)<TimeCreated SystemTime\\='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
"""(?i)<Computer>({host}[^<>]+)</Computer>"""
"""(?i)<Keywords>({result}[^<>]+)</Keywords>"""
"""(?i)<Data Name\\='(Caller)?ProcessName'>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<"""
"""(?i)<Data Name\\='(Caller)?ProcessId'>({process_id}[^<]+?)\s*<"""
"""(?i)<Execution ProcessID\\='({process_id}[^'"]+)"""
"""(?i)<EventID>({event_code}\d+)"""
"""(?i)<Data Name\\='TargetUserName'>(SYSTEM|({dest_user}[^<]+))<"""
"""(?i)<Data Name\\='TargetDomainName'>({dest_domain}[^<]+)<"""
"""(?i)<Data Name\\='LogonType'>({login_type}\d+)<"""
"""(?i)<Data Name\\='TargetUserSid'>({dest_user_sid}[^<]+)<"""
"""(?i)<Data Name\\='TargetLogonId'>({dest_login_id}[^<]+)<"""
"""(?i)<Data Name\\='SubjectUserSid'>(-|({user_sid}[^<>]+))<"""
"""(?i)<Data Name\\='SubjectUserName'>(-|({user}[^<>]+))<"""
"""(?i)<Data Name\\='SubjectDomainName'>(-|({domain}[^<>]+))<"""
"""(?i)<Data Name\\='SubjectLogonId'>(-|({login_id}[^<>]+))<"""
"""(?i)({event_name}An account was logged off)"""
]
DupFields = [
"""dest_user->user"""
"""dest_user_sid->user_sid"""
"""dest_login_id->login_id"""
"""dest_domain->domain"""
]


}
```