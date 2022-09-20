#### Parser Content
```Java
{
Name = cisco-cws-kv-http-session-webcatcode
    Vendor = Cisco
    Product = Cisco Cloud Web Security
    TimeFormat = "epoch_sec"
    Conditions = [ """ wbrs-score=""",""" webcat-code="""]
    Fields = [
      """(Info|CISCOIPORTWSA\-\d+):\s+({time}\d+)\.\d+\s+\d+\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+({proxy_action}\w+)\/({http_response_code}\d+)\s\d+\s({method}[^\s]+)\s({url}[^\s]+)""",
      """(Info|CISCOIPORTWSA\-\d+):\s+([^\s]+\s){6}(?:({protocol}\w+):\/{2}({web_domain}[^:\/]+)(:\d+)?({uri_path}\/[^?\s]+)?({uri_query}\?[^\s]+)?)""",
      """(Info|CISCOIPORTWSA\-\d+):\s+([^\s]+\s){7}"\w+\\({user}[^@"]+)(@({domain}[^"]+))?"""",
      """(Info|CISCOIPORTWSA\-\d+):\s+([^\s]+\s){7}("[^"]+"|\-)\s([^\s]+\s)(?:-|({mime}[^\s]+))\s(?:-|({action}[^\-\s]+))""",
      """\ss-ip=\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\ss-port=\s+({dest_port}\d+)""",
      """\swebcat-code=\s+"({category}[^"]+)"""",
      """\scs-bytes=\s+({bytes_out}\d+)""",
      """\ssc-bytes=\s+({bytes_in}\d+)""",
      """\scs-user-agent=\s+"(?:-|({user_agent}[^"]+))"""",
    ]
	ParserVersion = "v1.0.0"
  

}
```