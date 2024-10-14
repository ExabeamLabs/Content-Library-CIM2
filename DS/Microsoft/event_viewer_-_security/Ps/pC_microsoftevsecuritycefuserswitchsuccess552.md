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
  """\srt=({time}\d{13})"""
  """ahost=({host}[^\s]+)"""
  """dvchost=({dest_host}[\w\-.]+)"""
  """duser=({account}[\w\-\.]+(?:\w+)?\$?)\s+\w+="""
  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """dntdom=({domain}.+?)\s+\w+="""
  """OriginalAgentAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```