#### Parser Content
```Java
{
Name = akamai-ca-json-http-session-webactivity
  ParserVersion = v1.0.0
  Vendor = Akamai
  Product = Cloud Akamai
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""message":{""""
""""reqHost":""""
""""status":""""
""""reqPath":"""" 
]
  Fields = [
    """"start":"({time}\d{10})""",
    """"proto":"({protocol}[^"]+)""",
    """"status":"({http_response_code}\d+)""",
    """"cliIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"reqPort":"({dest_port}\d+)""",
    """"reqHost":"({web_domain}[^"\s]+)""",
    """"reqMethod":"({method}[^"]+)""",
    """"reqPath":"({uri_path}[^"]+)""",
    """"reqQuery":"({uri_query}[^"]+)""",
    """"edgeIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"bytes":"({bytes}\d+)""",
  ]


}
```