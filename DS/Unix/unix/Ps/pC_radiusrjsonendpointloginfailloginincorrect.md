#### Parser Content
```Java
{
Name = "radius-r-json-endpoint-login-fail-loginincorrect"
ExtractionType = json
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ radiusd["""
  """ Login incorrect """
]
Fields = [
  """exa_json_path=$.@timestamp,exa_field_name=time""",
  """exa_regex=\sradiusd\[\d+\]:\s*\(\d+\) Login ({result}incorrect) \(({failure_reason}[^\)]+)\):\s*\[({user}[\w\.\-]{1,40}\$?)[^\]]*\] \(from client ({src_host}[\w\-.]+) port ({src_port}\d+)\) ({account}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```