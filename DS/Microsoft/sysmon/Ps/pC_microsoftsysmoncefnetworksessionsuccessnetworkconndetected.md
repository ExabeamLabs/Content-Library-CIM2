#### Parser Content
```Java
{
Name = microsoft-sysmon-cef-network-session-success-networkconndetected
Vendor = "Microsoft"
Product = "Sysmon"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft Sysmon|Sysmon NXLog|"""
  """|sysmonTask-SYSMON_NETWORK_CONNECT|Network connection detected|"""
]
Fields = [
  """CEF:([^\|]*\|){5}({operation}[^\|]+)"""
  """({host}\S+) CEF:"""
  """\Wdvc=({host}[A-Fa-f:\d]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wrt=({time}\d{13})"""
  """\WeventId=({event_code}\d+)"""
  """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wspt=({src_port}\d+)"""
  """\Wdhost=({dest_host}[\w\-.]+)"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wdpt=({dest_port}\d+)"""
  """\Wcs3=((NT AUTHORITY|({domain}[^\s\\]+))\\+)?(NETWORK SERVICE|LOCAL|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\Wdntdom=(NT AUTHORITY|({domain}\S+))"""
  """\Wduser=(SYSTEM|LOCAL|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\Wdproc=(SYSTEM|FINANS|({process_path}({process_dir}.*?)({process_name}[^\\]+?)))\s+(\w+=|$)"""
  """\Wcs6=\{({process_guid}[^\}]+)"""
  """\Wdpid=({process_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```