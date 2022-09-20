#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-switch-success-4648-1
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Snare|"""
  """|Microsoft-Windows-Security-Auditing:4648|"""
]
Fields = [
  """({event_name}A logon was attempted using explicit credentials)"""
  """\sexternalId=({event_code}\d+)"""
  """\srt=({time}\d+)"""
  """\sdvc=({dest_ip}[a-fA-F:\d.]+)"""
  """\sdvchost=({dest_host}[^\s]+)"""
  """\sduser=({user}.+?)\s+\w+="""
  """\ssuser=({user}.+?)\s+\w+="""
  """\sduser=({account}.+?)\s+\w+="""
  """\sdntdom=({domain}[^\s]+)"""
  """\sduid=({login_id}[^\s]+)"""
  """dproc=(?: |({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+)))\s+\w+="""
  """\ssrc=({src_ip}[a-fA-F:\d.]+)"""
]
DupFields = [
  "dest_ip->host"
  "dest_host->host"
]
ParserVersion = "v1.0.0"


}
```