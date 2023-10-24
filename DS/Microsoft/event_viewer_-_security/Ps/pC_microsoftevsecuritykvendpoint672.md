#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=672"""
]
Fields = [
  """EventID=({event_code}\d+).+?Supplied Realm Name:\s+({domain}[^\s]+)"""
  """TimeGenerated=({time}\d{10})"""
  """Computer=({host}[^\s]+)"""
  """User Name:\s+({user}[\w\.\-]{1,40}\$?)\s+Supplied Realm Name:.+?Result Code:\s+({result_code}.+?)\s.+Client Address:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```