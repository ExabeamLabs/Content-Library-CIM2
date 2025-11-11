#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-success-4624-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<EventID>4624<"""
"""An account was successfully logged on"""
"""<Data Name\="""
"""WorkstationName"""
]
Fields = [
"""<TimeCreated SystemTime\\=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
"""<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""<Provider Name\\=('|")({provider_name}[^'\"]+)"""
"""<EventID[^<]*?>({event_code}\d+)"""
"""({event_name}An account was successfully logged on)"""
"""<Data Name\\=('|")SubjectUserSid('|")>(-|({user_sid}.+?))<"""
"""<Data Name\\=('|")SubjectUserName('|")>(-|({user_upn}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_domain}({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+))?))|({full_name}[^\s<]+\s[^<]+)|(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>"""
"""<Data Name\\=('|")SubjectDomainName('|")>(-|({src_domain}({domain}.+?)))<"""
"""<Data Name\\=('|")SubjectLogonId('|")>(-|({login_id}.+?))<"""
"""<Data Name\\=('|")TargetUserName('|")>(SYSTEM|({dest_user}[^<]+))<"""
"""<Data Name\\=('|")TargetDomainName('|")>({dest_domain}[^<]+)<"""
"""<Data Name\\=('|")LogonType('|")>({login_type}\d+)<"""
"""<Data Name\\=('|")TargetUserSid('|")>({dest_user_sid}[^<]+)<"""
"""<Data Name\\=('|")TargetLogonId('|")>({dest_login_id}[^<]+)<"""
"""<Data Name\\=('|")ProcessName('|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<"""
"""<Data Name\\=('|")ProcessId('|")>({process_id}[^<]+?)\s*<"""
"""<Execution ProcessID\\=('|")({process_id}[^'\"]+)"""
"""<Data Name\\=('|")IpAddress('|")[^<>]*?>(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""<Data Name\\=('|")LogonProcessName('|")>({auth_process}[^\s<]+)"""
"""<Data Name\\=('|")AuthenticationPackageName('|")>({auth_package}[^<]+)<"""
"""<Data Name\\=('|")WorkstationName('|")>([A-Fa-f:\d.]+|-|({src_host}[^<]+))<"""
"""<Keywords>({result}.+?)</Keywords>"""
"""<Data Name\\=('|")WorkstationName('|")>([A-Fa-f:\d.]+|-|({src_host_windows}[^<]+))</Data>"""
"""<Data Name\\=('|")SubjectUserSid('|")>({subject_sid}[^<]+)</Data>"""
"""<Data Name\\=('|")KeyLength('|")>({key_length}\d+)</Data>"""
]
ParserVersion = "v1.0.0"


}
```