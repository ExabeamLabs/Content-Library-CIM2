#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """|Security:672|"""
]
Fields = [
  """({event_name}Account Logon)"""
  """({event_code}672)"""
  """\srt=({time}\d{13})"""
  """src=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\ssuser=({user}.+?)\s+\w+="""
  """\scs4=({result_code}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdntdom=({domain}[^\s]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```