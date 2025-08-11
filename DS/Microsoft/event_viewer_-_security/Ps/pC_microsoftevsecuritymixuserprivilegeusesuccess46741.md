#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-privilege-use-success-4674-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
Conditions = [
  """An operation was attempted on a privileged object"""
  """Computer"""
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)"""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """TimeGenerated=({time}\d{10})"""
  """TimeGenerated=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{7}Z)"""
  """Keywords=({result}[^=]+)\s+"""
  """Type\s*=\s*"({result}[^";]+)""""
  """"computer_name":"({host}[\w\-\.]+)""""
  """"ip":\[?("[^"]*",?)*\]?,"name":"({src_host}[\w\-\.]+)""""
  """"ip":\[?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"mac":\[?"({src_mac}[^"]+)""""
  """OriginatingComputer(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*"""
  """Computer(\w+)?["\s]*(:|=)\s*"?({host}[^\d]+?[\w\-.]+)"""
  """({event_code}4674)"""
  """"Account":"((NT AUTHORITY|({domain}[^\\\s"]+))\\+)?(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*""""
  """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)"""
  """Subject(:|=).*?Security ID(:|=)\s*({user_sid}.+?)[\s;]*Account Name"""
  """"SubjectUserSid":"({user_sid}[^\s"]+)"""
  """"SubjectLogonId":"({login_id}[^\s"]+)"""
  """"ObjectServer":"(-|({object_server}[^\s"]+))"""
  """"ObjectName":"(-|({object}[^\s"]+))"""
  """"ObjectType":"(-|({object_type}[^\s"]+))"""
  """Process\s*Name(:|=)\s*((?-i)\\+[rnt])*(?: |({process_path}({process_dir}(?:[^";]+?)?[\\\/])?({process_name}[^\\\/";]+?)))[\\n\s;]*Requested"""
  """\s*Account Name(:|=)\s*((?-i)\\+[rnt])*(?:-|(?i)local service|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+?))[\s;]*((?-i)\\+[rnt])*Account Domain(:|=)\s*((?-i)\\+[rnt])*((?i)NT AUTHORITY|({domain}.+?))[\s;]*((?-i)\\+[rnt])*Logon ID(:|=)\s*((?-i)\\+[rnt])*({login_id}.+?)[\s;]*((?-i)\\+[rnt])*Object(:|=)"""
  """\s*Object Server(:|=)\s*((?-i)\\+[rnt])*({object_server}.+?)[nrt\\\s;]*((?-i)\\+[rnt])*Object Type(:|=)\s*((?-i)\\+[rnt])*(?:-|({object_type}.+?))[\s;]*((?-i)\\+[rnt])*Object Name(:|=)\s*((?-i)\\+[rnt])*(?:|-|({object}.+?))[nrt\\\s;]*((?-i)\\+[rnt])*Object Handle"""
  """Desired Access(:|=)\s*((?-i)\\+[rnt])*({access}.+?)[\s;]*((?-i)\\+[rnt])*Privileges(:|=)\s*((?-i)\\+[rnt])*({privileges}.+?)(\s+\d+|"|,|;|\s+User:|\s*$)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```