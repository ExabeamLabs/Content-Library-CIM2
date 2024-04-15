#### Parser Content
```Java
{
Name = "radius-r-json-endpoint-login-fail-loginincorrect"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ radiusd["""
  """ Login incorrect """
]
Fields = [
  """"@timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """ radiusd\[\d+\]:\s*\(\d+\) Login ({result}incorrect) \(({failure_reason}[^\)]+)\):\s*\[({user}[^\s\/\]]+)[^\]]*\] \(from client ({src_host}[\w\-.]+) port ({src_port}\d+)\) ({account}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```