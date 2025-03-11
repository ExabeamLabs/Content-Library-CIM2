#### Parser Content
```Java
{
Name = "cisco-fp-kv-http-session-sfims"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """SFIMS"""
  """Policy: Default Access Control"""
  """ApplicationProtocol: HTTP"""
]
Fields = [
  """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """SrcPort:\s*({src_port}\d+)"""
  """DstPort:\s*({dest_port}\d+)"""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """AccessControlRuleAction:\s*({action}[^,]+)"""
  """UserName:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """Client:\s*({user_agent}[^,]+)"""
  """UserAgent:\s*({user_agent}.+?),\s*Client:"""
  """ApplicationProtocol:\s*({protocol}[^,]+)"""
  """InitiatorBytes:\s*({bytes_out}\d+)"""
  """ResponderBytes:\s*({bytes_in}\d+)"""
  """URLCategory:\s*({category}[^,]+)"""
  """URL:\s*({url}\S+?)(,\s*\w+:|\s)"""
  """URL:\s*(?:-|\w+:\/+)({web_domain}[^\s\/]+),?"""
  """URL:\s*(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)"""
  """URL:\s*.*?({uri_query}\?[^\s\"]+)"""
]
ParserVersion = "v1.0.0"


}
```