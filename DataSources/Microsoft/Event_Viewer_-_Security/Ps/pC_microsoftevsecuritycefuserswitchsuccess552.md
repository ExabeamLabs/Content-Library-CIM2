#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-switch-success-552
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Snare|"""
  """|Security:552|Logon attempt using explicit credentials|"""
]
Fields = [
  """({event_name}Logon attempt using explicit credentials)"""
  """({event_code}552)"""
  """rt=({time}\d+)"""
  """ahost=({host}[^\s]+)"""
  """dvchost=({dest_host}[^\s]+)"""
  """duser=({account}[\w\-\.]+(?:\w+)?\$?)\s+\w+="""
  """suser=({user}[\w\-\.\s]+(?:\w+)?\$?)\s+\w+="""
  """dntdom=({domain}.+?)\s+\w+="""
  """OriginalAgentAddress=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
  """dvc=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```