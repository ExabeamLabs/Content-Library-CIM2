#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-success-mcafee"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-26304624"""
]
Fields = [
  """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
  """({event_name}An account was successfully logged on)"""
  """\srt=({time}\d{13})"""
  """shost=({host}[\w\-.]+)"""
  """src=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
  """nitroAppID=({auth_package}.+?)\s+\w+="""
  """sntdom=({domain}.+?)\s+\w+="""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """duser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """nitroLogon_Type=({login_type}\d+)"""
  """nitroDestination_Logon_ID=({login_id}.+?)(\s|0\||\))"""
  """nitroSecurity_ID=({user_sid}[^\s]+)\s\w+="""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```