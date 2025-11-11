#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-endpoint-672"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "E MMM dd HH:mm:ss yyyy"
Conditions = [
  """Service Name:"""
  """krbtgt"""
  """(672)"""
]
Fields = [
  """EvntSLog:\s+\[.+\]\s+({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+):\s+({dest_host}({host}[\w.\- /\\]+))\/.*\s+\(({event_code}\w+)\)"""
  """User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Supplied Realm Name:\s+({domain}[^\s]+)"""
  """Client Address:\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Result Code:\s+({result_code}[\w\-]+)"""
  """User ID:\s\%\{({user_sid}[^}]+)\}"""
]
ParserVersion = "v1.0.0"


}
```