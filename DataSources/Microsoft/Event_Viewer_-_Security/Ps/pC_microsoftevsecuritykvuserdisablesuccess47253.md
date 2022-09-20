#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-disable-success-4725-3
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-26304725"""
]
Fields = [
  """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
  """({event_name}A user account was disabled)"""
  """\srt=({time}\d+)"""
  """shost=({host}[^\s]+)"""
  """sntdom=({domain}[^\s]+)"""
  """suser=({user}.+?)\s+\w+="""
  """duser=({dest_user}.+?)\s+\w+="""
  """nitroSource_Logon_ID=({login_id}[^\s]+)"""
  """nitroSecurity_ID=({user_sid}[^\s]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```