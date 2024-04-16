#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-success-4624"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """<EventID>4624</EventID>"""
  """<Data Name"""
  """'LogonType'"""
  ]
  Fields = [
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Data Name\\*=('|")ProcessId('|")>({process_id}[^<]+?)\s*<"""
  """<Provider Name\\*=('|")({provider_name}[^'\"]+)"""
  """({event_name}An account was successfully logged on)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}({dest_host}[\w\-.]+))<"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<EventID>({event_code}[^<]+)<"""
  """<Data Name\\*=('|")LogonType('|")>({login_type}\d+)<"""
  """<Data Name(\\)?=('|")TargetUserName('|")>(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@<=]+))?)</Data>"""
  """New Logon:[\s\S]*?Account Name:\s*((\\)[rnt])*(-|({account}[^\s:\\]*))((\\)[rnt])*\s*[\w\s]+""",
  """<Data Name\\*=('|")TargetDomainName('|")>(-|({domain}[^<]+))<"""
  """<Data Name\\*=('|")ProcessName('|")>(?:-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))<"""
  """<Data Name\\*=('|")IpAddress('|")[^<>]*?>(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)<"""
  """<Data Name\\*=('|")IpPort('|")>({src_port}\d+)"""
  """<Data Name\\*=('|")LogonProcessName('|")>({auth_process}[^\s<]+)"""
  """<Data Name\\*=('|")AuthenticationPackageName('|")>({auth_package}[^<]+)<"""
  """<Data Name\\*=('|")LmPackageName('|")>(-|({auth_package}[^<]+))<"""
  """<Data Name\\*=('|")TargetLogonId('|")>({login_id}[^<]+)<"""
  """<Data Name\\*=('|")TargetUserSid('|")>({user_sid}[^<]+)<"""
  """<Data Name\\*=('|")WorkstationName('|")>([A-Fa-f:\d.]+|-|({src_host_windows}[^<]+?))\s*<"""
  """EventRecordID>({event_id}[^<]+)<"""
  """<Keywords>({result}.+?)</Keywords>"""
  """<Data Name\\*=('|")SubjectUserSid('|")>({subject_sid}[^<]+)<"""
  """<Data Name\\*=('|")KeyLength('|")>({key_length}\d+)<"""
  """<Opcode>({result_code}\d+)<"""
  """Logon Type:\s*({login_type}\d+)"""
  """<Level>({run_level}[^<]+)<"""
  ]
  DupFields = [ "login_id->dest_login_id" , "user_sid->dest_user_sid" , "domain->dest_domain", "src_host_windows->src_host"]
  ParserVersion = "v1.0.0"


}
```