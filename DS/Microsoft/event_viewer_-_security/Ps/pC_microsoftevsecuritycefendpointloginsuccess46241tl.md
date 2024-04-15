#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-success-4624-1-tl"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<eventid>4624<"""
"""an account was successfully logged on"""
"""<data name\="""
"""workstationname"""
]
Fields = [
"(?i)<TimeCreated SystemTime\\='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{3})"
"(?i)<Computer>({host}[^<>]+)</Computer>"
"(?i)<Provider Name\\='({provider_name}[^'\"]+)"
"(?i)<EventID[^<]*?>({event_code}\\d+)"
"(?i)({event_name}An account was successfully logged on)"
"(?i)<Data Name\\='SubjectUserSid'>(-|({user_sid}.+?))<"
"(?i)<Data Name\\='SubjectUserName'>(-|({user}.+?))<"
"(?i)<Data Name\\='SubjectDomainName'>(-|({domain}.+?))<"
"(?i)<Data Name\\='SubjectLogonId'>(-|({login_id}.+?))<"
"(?i)<Data Name\\='TargetUserName'>(SYSTEM|({dest_user}[^<]+))<"
"(?i)<Data Name\\='TargetDomainName'>({dest_domain}[^<]+)<"
"(?i)<Data Name\\='LogonType'>({login_type}\\d+)<"
"(?i)<Data Name\\='TargetUserSid'>({dest_user_sid}[^<]+)<"
"(?i)<Data Name\\='TargetLogonId'>({dest_login_id}[^<]+)<"
"(?i)<Data Name\\='ProcessName'>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<"
"(?i)<Data Name\\='ProcessId'>({process_id}[^<]+?)\\s*<"
"(?i)<Execution ProcessID\\='({process_id}[^'\"]+)"
"(?i)<Data Name\\='IpAddress'[^<>]*?>(-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?)"
"(?i)<Data Name\\='LogonProcessName'>({auth_process}[^\\s<]+)"
"(?i)<Data Name\\='AuthenticationPackageName'>({auth_package}[^<]+)<"
"(?i)<Data Name\\='WorkstationName'>([A-Fa-f:\\d.]+|-|({src_host}[^<]+))<"
"(?i)<Keywords>({result}.+?)</Keywords>"
"(?i)<Data Name\\=('|\")WorkstationName('|\")>([A-Fa-f:\\d.]+|-|({src_host_windows}[^<]+))</Data>"
"(?i)<Data Name\\=('|\")SubjectUserSid('|\")>({subject_sid}[^<]+)</Data>"
"(?i)<Data Name\\=('|\")KeyLength('|\")>({key_length}\\d+)</Data>"
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```