#### Parser Content
```Java
{
Name = zeek-z-json-http-session-status
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ 
""""status_code":"""
""""trans_depth":"""
""""id.resp_h":"""
""""resp_mime_types""""
]
  Fields = [
    """"ts\\?"+:[\[\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
    """"ts\\?"+:\\?"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid\\?"+:\\?"+({connection_id}[^"]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"proto\\?"+:\\?"+({protocol}[^"]+)""",
    """"_system_name":"({host}[^"]+)""",
    """"status_code":({http_response_code}\d+)""",
    """"resp_mime_types":\["({mime}[^"]+)""",
    """"resp_fuids":\["({file_id}[^"]+)""",
    """"status_msg":"({additional_info}[^"]+)""",
    """"method":"({method}[^"]+)""",
    """"uri":"({uri_path}[^"\?]+?)\s*({uri_query}\?[^"]+?)?\s*"""",
    """"user_agent":"\s*({user_agent}[^"]+?)\s*""""
  ]


}
```