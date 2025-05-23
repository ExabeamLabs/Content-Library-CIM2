#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-share-access-success-5140"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSS", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd HH:mm:ss"]
Conditions = [ """A network share object was accessed""", """Account Name:""" ]
Fields = [
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
  """({event_name}A network share object was accessed)""",
  """({event_code}5140)""",
  """<Computer>(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))<\/Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))""",
  """(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\sMSWinEventLog""",
  """\sComputer(Name)?=\s*(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""",
  """"system_name":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """"(Hostname|Computer)":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
  """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
  """\sTimeGenerated=({time}\d{10})""",
  """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
  """\sEventReceivedTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+)))\s""",
  """({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Detailed File Share|File Share)""",
  """Logon ID:\s*((\\)*(\\r|\\t|\\n))*({login_id}\S+?)((\\)*(\\r|\\t|\\n))*\s*Network Information:""",
  """Account Name:\s*((\\)*(\\r|\\t|\\n))*({user}[\w\.\-\!\#\^\~]{1,40}\$?)((\\)*(\\r|\\t|\\n))*\s*Account Domain:"""
  """Security ID:\s*((\\)*(\\r|\\t|\\n))*({user_sid}[^\s]+)((\\)*(\\r|\\t|\\n))*\s*Account Name:""",
  """Account Domain:\s*((\\)*(\\r|\\t|\\n))*({domain}\S+?)((\\)*(\\r|\\t|\\n))*\s*Logon ID:""",
  """Object Type:\s*((\\)*(\\r|\\t|\\n))*({file_type}[^:]+?)((\\)*(\\r|\\t|\\n))*\s*Source Address:""",
  """Source Address:\s*((\\)*(\\r|\\t|\\n))*(::ffff:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+?))((\\)*(\\r|\\t|\\n))*\s*Source Port:""",
  """({access}Read)""",
  """Share Name:\s*((\\)*(\\r|\\t|\\n))*(?:\\\\\*\\)?({share_name}[^:]+?)((\\)*(\\r|\\t|\\n))*\s*Share Path:""",
  """Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?)))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:""",
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
  """Computer=\s*(::ffff:)?"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """Source Port:\s*({src_port}\d+)"""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
  """ShareName\\?"+:\\?"+[\\\*]*({share_name}[^\\"]+)"""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\"]+)\\?""""
  """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^\\]+))\\?""""
]
DupFields = [ "share_path->file_path", "src_user->user", "src_domain->domain" ]
ParserVersion = "v1.0.0"


}
```