#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-share-access-success-5140-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
Conditions = [ """A network share object was accessed""", """Account Name:""", """EventID="5140"""", """"Microsoft-Windows-Security-Auditing"""" ]
Fields = [
  """({event_name}A network share object was accessed)""",
  """({event_code}5140)""",
  """<Computer>(::ffff:)?({dest_host}({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({=dest_host}[\w\-.]+)))<\/Computer>""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))""",
  """(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\sMSWinEventLog""",
  """Computer(Name)?=\s*(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""",
  """"system_name":"(::ffff:)?({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))"""",
  """"Hostname":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """Event.System.TimeCreated _SystemTime="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
  """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+)))\s""",
  """({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Detailed File Share|File Share)""",
  """Logon ID:\s*((\\)*(\\r|\\t|\\n))*({login_id}\S+?)((\\)*(\\r|\\t|\\n))*\s*Network Information:""",
  """Account Name:\s*((\\)*(\\r|\\t|\\n))*({user}[\w\.\-\!\#\^\~]{1,40}\$?)((\\)*(\\r|\\t|\\n))*\s*Account Domain:"""
  """Account Domain:\s*((\\)*(\\r|\\t|\\n))*({domain}\S+?)((\\)*(\\r|\\t|\\n))*\s*Logon ID:""",
  """Object Type:\s*((\\)*(\\r|\\t|\\n))*({file_type}[^:]+?)((\\)*(\\r|\\t|\\n))*\s*Source Address:""",
  """Source Address:\s*((\\)*(\\r|\\t|\\n))*(::ffff:)?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+?))((\\)*(\\r|\\t|\\n))*\s*Source Port:""",
  """({access}Read)""",
  """Share Name:\s*((\\)*(\\r|\\t|\\n))*(?:[\\\*]+)?({share_name}[^:]+?)((\\)*(\\r|\\t|\\n))*\s*Share Path:""",
  """Share Path:\s*((\\)*(\\r|\\t|\\n))*(?:\\+\?+)(?:\s*|({file_path}({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?))))[\\\/]?)((\\)*(\\r|\\t|\\n))*\s*Access Request Information:""",
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
  """Computer=\s*(::ffff:)?"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """Source Port:\s*({src_port}\d+)"""
  """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?""""
  """ShareName\\?"+:\\?"+[\\\*]*({share_name}[^\\"]+)"""
  """SubjectLogonId\\?"+:\\?"+({login_id}[^\\"]+)\\?""""
  """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\]+)))\\?""""
]
ParserVersion = "v1.0.0"


}
```