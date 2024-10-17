#### Parser Content
```Java
{
Name = crowdstrike-falcon-kv-network-traffic-success-falconsensor
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CrowdStrike""" ,"""SslConnect: """, """falcon-sensor""" ]
  Fields = [
    """\d\d:\d\d\s({host}[\w\-\.]+)\s({log_source}[^\[]+)(\[\d+\]):(([^:]+):)?\sCrowdStrike[^"]*SslConnect:(\s({dest_host}[\w\-\.]+):({dest_port}\d+))?\s*(({additional_info}[^"]+?)$)?"""
  ]
  ParserVersion = "v1.0.0"


}
```