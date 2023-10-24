#### Parser Content
```Java
{
Name = zeek-z-json-http-session-hoststatus
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""""id.orig_h":"""
""""id.resp_h":"""
""""host":"""
""""method":"""
]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid":"({connection_id}[^"]+)""",
    """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p":({src_port}\d+)""",
    """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p":({dest_port}\d+)""",
    """"host":"(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}[^\s"]+\.[^\s"]+)|({host}[\w.-]+))""",
    """"_system_name":"({host}[^"]+)""",
    """"uri":"({uri_path}[^"\?]+?)\s*({uri_query}\?[^"]+?)?\s*"""",
    """"user_agent":"\s*({user_agent}[^:]+?)\s*",""",
    """"status_code":({http_response_code}\d+)""",
    """"method":"({method}[^"]+)""",
    """"resp_mime_types":\["({mime}[^"]+)""",
  ]


}
```