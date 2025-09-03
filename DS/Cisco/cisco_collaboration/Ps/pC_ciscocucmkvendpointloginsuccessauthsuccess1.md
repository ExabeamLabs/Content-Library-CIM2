#### Parser Content
```Java
{
Name = cisco-cucm-kv-endpoint-login-success-authsuccess-1
Vendor = Cisco
Product = Cisco Collaboration
TimeFormat = "MMM dd yyyy hh:mm:ss a"
Conditions = [
  """[Login Date/Time="""
  """[Login IP Address/Hostname="""
  """Login Authentication succeeded"""
]
Fields = [
  """Login Date/Time=({time}\d\d/\d\d/\d\d \d+:\d+ (am|pm|AM|PM))"""
  """\s({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+(AM|PM|am|pm))"""
  """Login IP Address/Hostname=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Login UserID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Node ID=({dest_host}[^\]]+)"""
  """Login Interface=({app}[^\]]+)"""
]
ParserVersion = "v1.0.0"


}
```