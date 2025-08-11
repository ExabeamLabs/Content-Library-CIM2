#### Parser Content
```Java
{
Name = sigsci-sigsci-json-http-session-uri
    ParserVersion = "v1.0.0"
    Vendor = SIGSCI
    Product = SIGSCI
    TimeFormat ="yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ 
  """serverHostname":"""
  """remoteHostname":"""
  """serverName":"""
  """uri":"""
  ]
    Fields = [
      """"+(serverHostname|serverName)"+:"+({dest_host}[\w\-.]+)"""",
      """"+remoteIP"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"+remoteHostname"+:"+(|({src_host}[\w\-.]+))"""",
      """"userAgent":"(|({user_agent}[^"]+))"""",
      """"+timestamp"+:"+({time}[^"]+)""",
      """"+method"+:"+({method}[^"]+)""",
      """"+path"+:"+({uri_path}[^"]+)""",
      """"+responseCode"+:({http_response_code}\d+)""",
      """"+(H|h)ost"+."+({host}[\w\-.]+?)(:\d+)?"""",
      """BLOCKED"*":\s*\{"+type"+:"+({action}[^"]+)""",
      """"+protocol"+:"+({protocol}\w+\/[^"]+)""",
      """"+Content-Type"+(:|,)"+({mime}[^";]+)""",
      """"+responseSize"+:({bytes_out}\d+)"""
      ]
  

}
```