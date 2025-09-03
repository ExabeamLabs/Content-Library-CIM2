#### Parser Content
```Java
{
Name = cisco-fp-kv-radius-traffic-success-113004
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd yyyy HH:mm:ss"]
Conditions = [
  """-113004"""
  """%FTD-"""
  """AAA user authentication Successful"""
]
Fields = [
  """({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s[\w\-\.]+\s*:\s*%FTD""",
  """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)"""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """%FTD-({priority}\d+)-({event_code}\d+)"""
  """server\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """-113004:\s*({event_name}AAA user authentication Successful)"""
  """user\s*=\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\s\/\\]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"


}
```