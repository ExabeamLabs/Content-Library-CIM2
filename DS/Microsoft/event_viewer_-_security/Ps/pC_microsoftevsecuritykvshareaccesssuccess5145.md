#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-share-access-success-5145"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """A network share object was checked to see whether the client can be granted desired access"""
  """(5145)"""
  """domain:"""
]
Fields = [
  """\d\d:\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s+(CEF|dsa_lca):"""
  """({event_name}A network share object was checked to see whether the client can be granted desired access)"""
  """({event_code}5145)"""
  """domain:\s+[^\s:]+:\s+({user_sid}[^\s]+)\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({domain}[^\s]+)\s+({login_id}[^\s]+)\s+({file_type}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+(?:[\\\*]+)?({share_name}[^\s]+)\s*(({share_path}[^\s]+)\s+({file_path}({file_dir}.*?[\\\/]+)?({file_name}[^\\\/]+?(\.({file_ext}\w+))?)?)\s+({access_mask}0x\d+)\s+({access}[^:]+?)\s+({access_reason}[\%\d]+:.+?)\s*)($|\w+=|"|')"""
]
ParserVersion = "v1.0.0"


}
```