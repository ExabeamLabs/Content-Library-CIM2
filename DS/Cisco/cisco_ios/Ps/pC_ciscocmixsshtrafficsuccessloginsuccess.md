#### Parser Content
```Java
{
Name = "cisco-c-mix-ssh-traffic-success-loginsuccess"
Vendor = "Cisco"
Product = "Cisco IOS"
TimeFormat = ["HH:mm:ss Z EEE MMM dd yyyy"]
Conditions = [
  """-LOGIN_SUCCESS:"""
]
Fields = [
  """at ({time}\d\d:\d\d:\d\d \w+ \w+ \w+ \d{1,2} \d\d\d\d)"""
  """\s\d\d:\d\d:\d\d\s({host}[^\s]+)\s"""
  """<\d+>[^:\s]+:\s+({host}[^:\s]+):"""
  """dvc=({host}[^\s]+)"""
  """\[user:\s*(({domain}[^\\\]\s]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """\[Source:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\[localport:\s*({src_port}\d+)"""
  """\s({event_code}\S+\d+-LOGIN_SUCCESS):"""
]
ParserVersion = "v1.0.0"


}
```