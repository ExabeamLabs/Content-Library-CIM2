#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-success-esm"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-21100552"""
]
Fields = [
  """({event_name}Logon attempt using explicit credentials)"""
  """\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
  """rt=({time}\d{13})"""
  """deviceTranslatedAddress=({host}[a-fA-F:\d.]+)"""
  """shost=({dest_host}[\w\-.]+)"""
  """duser=({dest_user}[\w\-\.]+(?:\w+)?\$?)\s+suser"""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+nitroSource"""
  """sntdom=({domain}.+?)\s+shost"""
  """nitroSource_Logon_ID=\([^,]+,({login_id}[^\)]+)"""
]
ParserVersion = "v1.0.0"


}
```