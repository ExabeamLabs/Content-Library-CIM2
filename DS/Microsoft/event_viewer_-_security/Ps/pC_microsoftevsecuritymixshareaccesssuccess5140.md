#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-share-access-success-5140"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [ """A network share object was accessed""", """Account Name:""" ]
Fields = [
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
  """({event_name}A network share object was accessed)""",
  """({event_code}5140)""",
  """(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\sMSWinEventLog""",
  """\sComputer(Name)?=\s*(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""",
  """<Computer>(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^<]+))<\/Computer>""",
  """"system_name":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """"Hostname":"(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
  """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(AM|PM))""",
  """"EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
  """\sTimeGenerated=({time}\d{10})""",
  """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)""",
  """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+)))""",
  """({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Detailed File Share|File Share)""",
  """Logon ID:\s*((\\)[rnt])*({login_id}\S+?)((\\)[rnt])*\s*Network Information:""",
  """Account Name:\s*((\\)[rnt])*({user}\S+?)((\\)[rnt])*\s*Account Domain:"""
  """Account Domain:\s*((\\)[rnt])*({domain}\S+?)((\\)[rnt])*\s*Logon ID:""",
  """Object Type:\s*((\\)[rnt])*({file_type}[^:]+?)((\\)[rnt])*\s*Source Address:""",
  """Source Address:\s*((\\)[rnt])*(::ffff:)?(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})+?))((\\)[rnt])*\s*Source Port:""",
  """({access}Read)""",
  """Share Name:\s*((\\)[rnt])*(?:\\\\\*\\)?({share_name}[^:]+?)((\\)[rnt])*\s*Share Path:""",
  """Share Path:\s*((\\)[rnt])*(?:\\+\?+)(?:\s*|({share_path}(({d_parent}[^"]+?)[\\\/])?(|({d_name}[^\\\/]+?)))[\\\/]?)((\\)[rnt])*\s*Access Request Information:""",
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""
  """Computer=\s*(::ffff:)?"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))"""",
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```