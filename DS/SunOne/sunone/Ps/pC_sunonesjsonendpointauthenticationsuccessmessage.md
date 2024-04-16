#### Parser Content
```Java
{
Name = sunone-s-json-endpoint-authentication-success-message
  Vendor = SunOne
  Product = SunOne
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"message":"A client attempted to access the server using SMB1."""" ]
  Fields = [
    """"@timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
    """"index":"[^\{\}]*?"host":"({host}[\w\-.]+)""",
    """"host":"({host}[\w\-.]+)"[^\{\}]*?"index":"""",
    """"destination":\{.*?"ipv4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"destination":\{.*?"host":"({dest_host}[\w\-.]+)""",
    """"source":\{.*?"ipv4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"source":\{.*?"host":"({src_host}[\w\-.]+)""",
    """"message":"({event_name}[^"]+)""",
  ]



}
```