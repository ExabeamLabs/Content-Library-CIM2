#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-privilege-use-success-4674"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
  """An operation was attempted on a privileged object"""
]
Fields = [
  """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))\s""",
  """({event_name}An operation was attempted on a privileged object)"""
  """({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))"""
  """\scategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)"""
  """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
  """TimeGenerated=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
  """Event Type\s*:\s*({result}.+?)\.\s+Log Type""",
  """Keywords=({result}.+?);?\s*Message=""",
  """Type\s*=\s*"({result}[^";]+)""""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))"""
  """({event_code}4674)""",
  """\s*Source Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Source Port(:|=)"""
  """({event_code}4674)"""
  """Process Name(:|=)\s*(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Requested"""
  """\s*Account Name(:|=)\s*(?:-|(?i)local service|({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+?))[\s;]*Account Domain(:|=)\s*({domain}.+?)[\s;]*Logon ID(:|=)\s*({login_id}.+?)[\s;]*Object(:|=)"""
  """\s*Object Server(:|=)\s*({object_server}.+?)[nrt\\\s;]*Object Type(:|=)\s*(?:-|({object_type}.+?))[\s;]*Object Name(:|=)\s*(?:|-|({object}.+?))[nrt\\\s;]*Object Handle"""
  """Desired Access(:|=)\s*({access}.+?)[\s;]*Privileges(:|=)\s*({privileges}.+?)(\s+\d+|"|,|;|\s+User:|\s$)"""
  """"Account":"((NT AUTHORITY|({domain}[^\\\s"]+))\\+)?(LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))\s*""""
  """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectServer":"(-|({object_server}[^\s"]+))"""
  """"ObjectName":"(-|({object}[^\s"]+))"""
  """"ObjectType":"(-|({object_type}[^\s"]+))"""
  """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*""""
]
ParserVersion = "v1.0.0"


}
```