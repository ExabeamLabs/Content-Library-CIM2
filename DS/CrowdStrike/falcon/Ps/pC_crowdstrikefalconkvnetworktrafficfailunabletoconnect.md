#### Parser Content
```Java
{
Name = crowdstrike-falcon-kv-network-traffic-fail-unabletoconnect
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CrowdStrike""" ,"""SslConnect: Unable to connect""", """falcon-sensor""", """via Application Proxy:""" ]
  Fields = [
    """\d\d:\d\d\s({host}[\w\-\.]+)\s({log_source}[^\[]+)(\[\d+\]):\sCrowdStrike[^"]*SslConnect: ({additional_info}Unable to connect to\s({dest_host}[\w\-\.]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```