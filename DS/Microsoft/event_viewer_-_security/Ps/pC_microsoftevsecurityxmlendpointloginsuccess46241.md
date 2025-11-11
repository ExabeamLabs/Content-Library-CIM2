#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-success-4624-1"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """<EventID>4624</EventID>"""
  """<Data Name"""
  """"LogonType""""
  ]
  Fields = [
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_name}An account was successfully logged on)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}({dest_host}[\w\-.]+))<"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}[^<]+)<"""
  """<Data Name\\*=('|")LogonType('|")>({login_type}\d+)<"""
  """<Data Name(\\)?=('|")TargetUserName('|")>(({dest_email_address}({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({dest_domain}({domain}[^@<=]+)))?)</Data>"""
  """<Data Name\\*=('|")TargetUserName('|")>(-|({user_upn}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_domain}({domain}[^\]\s"\\,;\|]+(\.[^\]\s"\\,;\|]+))?))|({full_name}[^\s<]+\s[^<]+)|(SYSTEM|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))<\/Data>"""
  """<Data Name\\*=('|")TargetDomainName('|")>(-|({dest_domain}({domain}[^<]+)))<"""
  """<Data Name\\*=('|")ProcessName('|")>(?:-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<"""
  """<Data Name\\*=('|")IpAddress"[^<>]*?>(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)<""",
  """<Data Name\\*=('|")IpPort('|")>({src_port}\d+)""",
  """<Data Name\\*=('|")LogonProcessName('|")>({auth_process}[^\s<]+)"""
  """<Data Name\\*=('|")AuthenticationPackageName('|")>({auth_package}[^<]+)<"""
  """<Data Name\\*=('|")LmPackageName('|")>(-|({auth_package}[^<]+))<"""
  """<Data Name\\*=('|")TargetLogonId('|")>({login_id}[^<]+)<"""
  """<Data Name\\*=('|")TargetUserSid('|")>({dest_user_sid}({user_sid}[^<]+))<"""
  """<Data Name\\*=('|")WorkstationName('|")>([A-Fa-f:\d.]+|-|({src_host_windows}({src_host}[\w\-\.]+?)))\s*<"""
  """EventRecordID>({event_id}[^<]+)<"""
  """<Data Name\\*=('|")SubjectUserSid('|")>({subject_sid}[^<]+)<"""
  """<Data Name\\*=('|")KeyLength('|")>({key_length}\d+)<"""
  """<Data Name\\*=('|")ProcessId('|")>({process_id}[^<]+?)\s*<"""
  """<Provider Name\\*=('|")({provider_name}[^'\"]+)"""
  """<Keywords>({result}.+?)</Keywords>"""
  """<Data Name(\\)?=('|")ObjectName('|")>({object}[^<>]+)<"""
  """<Level>({run_level}[^<]+)<"""
  """Linked Logon ID(:|=)\s*(\\[nrt])*({dest_login_id}[^\s\\;]+)\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```