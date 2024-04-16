#### Parser Content
```Java
{
Name = "radius-r-json-vpn-login-success-loginok"
ExtractionType = json
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ radiusd["""
  """ Login OK"""
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time""",
  """exa_regex=\sradiusd\[\d+\]:\s*\(\d+\) Login ({result}OK):\s*\[({user}[\w\.\-]{1,40}\$?)\] \(from client ({src_host}[\w\-.]+) port ({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```