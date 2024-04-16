#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-share-access-5145-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """A network share object was checked to see whether client can be granted desired access"""
  """Account Name:"""
  """EventCode=5145"""
]
Fields = [
  """({event_name}A network share object was checked to see whether client can be granted desired access)"""
  """({event_code}5145)"""
  """({host}[\w\-.]+)\s+(?i)((audit|success)( |_)(success|audit))""",
  """(::ffff:)?(Unknown|({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))))\s+(?i)((audit|success)( |_)(success|audit))"""
  """({time}\d\d\/\d\d\/\d{1,4} \d\d:\d\d:\d\d (am|AM|pm|PM))"""
  """(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s"""
  """Logon ID:\s*((\\)[rnt])*({login_id}\S+?)((\\)[rnt])*\s*Network Information:"""
  """Account Name:\s*((\\)[rnt])*({user}[\w\.\-]{1,40}\$?)((\\)[rnt])*\s*Account Domain:"""
  """Account Domain:\s*((\\)[rnt])*({domain}\S+?)((\\)[rnt])*\s*Logon ID:"""
  """Object Type:\s*((\\)[rnt])*({file_type}.+?)((\\)[rnt])*(\s*|[\s,]*)Source Address:"""
  """Source Address:\s*((\\)[rnt])*(::1|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)((\\)[rnt])*\s*Source Port:"""
  """Share Name:\s*((\\)[rnt])*(?:\\\\\*\\)?({share_name}[^=]+?)((\\)[rnt])*\s*Share Path:""",
  """Share Name:\s*((\\)[rnt])*(?:\\\\\*\\)?({share_name}.+?)((\\)[rnt])*\s*Share Path:"""
  """Share Path:\s*((\\)[rnt])*(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}[^=]+?)\\)?(|({d_name}[^\\]*?)))\\?)((\\)[rnt])*(,|\s)\s*Relative Target Name:"""
  """Relative Target Name:\s*((\\)[rnt])*\\?(?:\s*|(?:({file_dir}[^=]+)\\)?(|({file_name}[^\\:\/]+?(?:\.({file_ext}[^\.]+?))?))(?:\\HEAD|:[^=]+?|\\|\s|((\\)[rnt])*)\s*)Access Request Information:""",
  """Share Path:\s*((\\)[rnt])*(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+?)\\)?(|({d_name}[^\\]*?)))\\?)((\\)[rnt])*(,|\s)\s*Relative Target Name:"""
  """Relative Target Name:\s*((\\)[rnt])*\\?(?:\s*|(?:({file_dir}.+?)\\)?(|({file_name}[^\\:\/]+?(?:\.({file_ext}[^\.\\]+?))?))(?:\\HEAD|:.+?|\\|\s|((\\)[rnt])*))(\s|[,\s]*)\s*Access Request Information:"""
  """Accesses:.*({access}SYNCHRONIZE|Execute|Traverse|Read|READ|WRITE_DAC|WRITE_OWNER|WriteAttributes|WriteEA|WriteData|AppendData|delete|Delete).*Access Check Results:"""
  """Keywords=({result}Audit Success|Success Audit|Audit Failure|Failure Audit)"""
  """Access Check Results:\s*[^=]*({result}-)\s""",
  """Access Check Results:[^=]*({result}Granted|Denied)\s+by"""
  """(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s"""
  """Source Port(=|:)\s*({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```