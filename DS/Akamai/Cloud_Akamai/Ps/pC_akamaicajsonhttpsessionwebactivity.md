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
    """"start":"({time}\d+)""",
    """"proto":"({protocol}[^"]+)""",
    """"status":"({http_response_code}\d+)""",
    """"cliIP":"({src_ip}[A-Fa-f:\d.]+)""",
    """"reqPort":"({dest_port}\d+)""",
    """"reqHost":"({web_domain}[^"\s]+)""",
    """"reqMethod":"({method}[^"]+)""",
    """"reqPath":"({uri_path}[^"]+)""",
    """"reqQuery":"({uri_query}[^"]+)""",
    """"edgeIP":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"bytes":"({bytes}\d+)""",
  ]


}
```