#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-share-access-success-5140-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [ """<EventID>5140</EventID>""", """ ThreadID=""", """Microsoft-Windows-Security-Auditing""" ]
Fields = [
  """({event_name}A network share object was accessed)""",
  """<EventID>({event_code}5140)""",
  """<Computer>({host}({dest_host}[\w\-.]+))</Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """<TimeCreated SystemTime(\\\/)?=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d*Z('|")/>""",
  """<Data Name(\\\/)?=('|")SubjectLogonId('|")>({login_id}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
  """<Data Name(\\\/)?=('|")SubjectDomainName('|")>({domain}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")SubjectUserName('|")>(-|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
  """<Data Name(\\\/)?=('|")SubjectDomainName('|")>({src_domain}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")ObjectType('|")>({file_type}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")IpAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>""",
  """<Data Name(\\\/)?=('|")ShareName('|")>(?:[\\\*]*)?({share_name}[^<]+?)</Data>""",
  """<Data Name(\\\/)?=('|")ShareLocalPath('|")>(?:[\\\\/?]+)?(|({share_path}({d_parent}[^<]+?[\\\/])?({d_name}[^\\\/<]+?)?[\\\/]?))</Data>""",
  """({access}4416)""",
  """<Data Name(\\\/)?=('|")AccessList('|")>(%%)?({access}[\d\w]+)"""
  """('|")IpPort('|")>({src_port}\d+)"""
  """Logon ID:\s*((\\)*(\\r|\\t|\\n))*({login_id}\S+?)((\\)*(\\r|\\t|\\n))*\s*Network Information:""",
  """Account Name:\s*((\\)*(\\r|\\t|\\n))*({user}[\w\.\-\!\#\^\~]{1,40}\$?)((\\)*(\\r|\\t|\\n))*\s*Account Domain:"""
  """Account Domain:\s*((\\)*(\\r|\\t|\\n))*({domain}\S+?)((\\)*(\\r|\\t|\\n))*\s*Logon ID:""",
  """Object Type:\s*((\\)*(\\r|\\t|\\n))*({file_type}[^:]+?)((\\)*(\\r|\\t|\\n))*\s*Source Address:""",
  """Source Address:\s*((\\)*(\\r|\\t|\\n))*(::ffff:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+?))((\\)*(\\r|\\t|\\n))*\s*Source Port:""",
  """({access}Read)""",
  """Share Name:\s*((\\)*(\\r|\\t|\\n))*(?:\\\\\*\\)?({share_name}[^:]+?)((\\)*(\\r|\\t|\\n))*\s*Share Path:""",
  """Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?)))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:""",
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
  """Computer=\s*(::ffff:)?"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """Source Port:\s*({src_port}\d+)"""
  """<Level>({run_level}[^<]+)<"""
]
DupFields = [
  "host->dest_host"
  "share_path->file_path"
]
ParserVersion = "v1.0.0"


}
```