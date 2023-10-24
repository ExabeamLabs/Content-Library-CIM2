#### Parser Content
```Java
{
Name = "cisco-iws-kv-http-session-accesslog"
Vendor = "Cisco"
Product = "IronPort Web Security"
TimeFormat = "yyyy-dd-MM HH:mm:ss.SSS"
Conditions = [
  """xb-accesslog: Info"""
]
Fields = [
  """Info:\s.*?\s({src_ip}\d+.\d+.\d+.\d+)\s({proxy_action}[^\/\s]+)\/({http_response_code}\d+)\s\d+\s({method}[^\s]+)\s((({dest_ip}\d+.\d+.\d+.\d+):({dest_port}\d+)\s)|({url}[^\s]+))?.+?\sDIRECT\/({web_domain}[^\s]+)"""
  """User\sAgent\s=\s(-,\s|\"*({user_agent}[^\"=]+))"""
  """<\d+>\w+ \d+ \d+:\d+:\d+\s+({host}[^\s]+) xb-accesslog: Info:"""
  """"(-|({event_category}[^\"]+?))\",([^,]+?,){19}->"""
]
ParserVersion = "v1.0.0"


}
```