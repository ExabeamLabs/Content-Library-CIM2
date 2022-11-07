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
  """\Wrt=({time}\d+)"""
  """\WeventId=({event_code}\d+)"""
  """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\Wsrc=({src_ip}[A-Fa-f:\d.]+)"""
  """\Wspt=({src_port}\d+)"""
  """\Wdhost=({dest_host}[\w\-.]+)"""
  """\Wdst=({dest_ip}[A-Fa-f:\d.]+)"""
  """\Wdpt=({dest_port}\d+)"""
  """\Wcs3=((NT AUTHORITY|({domain}[^\s\\]+))\\+)?(NETWORK SERVICE|LOCAL|SYSTEM|({user}[^\s\\]+))"""
  """\Wdntdom=(NT AUTHORITY|({domain}\S+))"""
  """\Wduser=(SYSTEM|LOCAL|NETWORK SERVICE|({user}[^\s]+))"""
  """\Wdproc=(SYSTEM|FINANS|({process_path}({process_dir}.*?)({process_name}[^\\]+?)))\s+(\w+=|$)"""
  """\Wcs6=\{({process_guid}[^\}]+)"""
  """\Wdpid=({process_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```