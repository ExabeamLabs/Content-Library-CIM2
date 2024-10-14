#### Parser Content
```Java
{
Name = "trendmicro-officescan-leef-user-privilege-use-success-4674"
Vendor = "Trend Micro"
Product = "OfficeScan"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LEEF:"""
  """|Trend Micro|Deep Security Agent|"""
  """cat=Log Inspection"""
  """An operation was attempted on a privileged object"""
  """(4674)"""
]
Fields = [
  """\d\d:\d\d:\d\d ({host}[\w\-.]+) LEEF:"""
  """dvc=({host}[A-Fa-f:\d.]+)"""
  """shost=({src_host}[\w\-.]+)"""
  """({event_code}4674)"""
  """({event_name}An operation was attempted on a privileged object)"""
  """Security:\s*({result}[^\(]+)"""
  """Process Name:\s*(?: |({process_path}({process_dir}(?:[^\"]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\s*Requested"""
  """Account Name:\s*(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:"""
  """Account Domain:\s*({domain}.+?)\s*Logon ID:"""
  """Logon ID:\s*({login_id}.+?)\s*Object:"""
  """Object Server:\s*({object_server}.+?)\s*Object Type:"""
  """Object Type:\s*(?:-|({object_type}.+?))\s*Object Name:"""
  """Object Name:\s*(?:-|({object}.+?))\s*Object Handle"""
  """Desired Access:\s*({access}.+?)\s*Privileges:"""
  """Privileges:\s*({privileges}\S+)"""
]
ParserVersion = "v1.0.0"


}
```