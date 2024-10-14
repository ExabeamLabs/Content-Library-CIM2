#### Parser Content
```Java
{
Name = "kemp-loadmaster-str-app-activity-success-user"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """l7log:"""
  """User """
  """ requested GET """
]
Fields = [
  """\s({host}[\w\-\.]+?)\s+\w+\d+\s+\-\s+l7log:"""
  """\d+log:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({dest_port}\d+):\s*\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)\)"""
  """\sUser\s*\'(({domain}[^']+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\'"""
  """\sUser\s*\'({email_address}[^\s@]+@[^\s@]+)\'"""
  """\sUser\s*\'({user}[\w\.\-\!\#\^\~]{1,40}\$?)\'"""
  """\srequested ({operation}GET) ({object}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```