#### Parser Content
```Java
{
Name = "radius-r-json-vpn-login-success-loginok"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ radiusd["""
  """ Login OK"""
]
Fields = [
  """"@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """ radiusd\[\d+\]:\s*\(\d+\) Login ({result}OK):\s*\[({user}[\w\.\-]{1,40}\$?)\] \(from client ({src_host}[\w\-.]+) port ({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```