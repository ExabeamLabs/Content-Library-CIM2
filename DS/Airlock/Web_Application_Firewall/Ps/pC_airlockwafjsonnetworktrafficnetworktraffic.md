#### Parser Content
```Java
{
Name = airlock-waf-json-network-traffic-networktraffic
  ParserVersion = v1.0.0
  Vendor = Airlock
  Product = Web Application Firewall
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"vhost_proto":"""", """"entry_url":"""", """"entry_query":"""", """"entry_path":"""", """"http_status":"""", """"vhost":"""" ]
  Fields = [
    """({time}\d+\-\d+\-\d+T\d+:\d+:\d+)\.\d+[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s+\{""",
    """"action":"({action}[^"]+)""",
    """"vhost_proto":"({protocol}[^"]+)""",
    """"vhost_port":"({dest_port}\d+)""",
    """"vhost_ip":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"vhost":"({dest_host}[\w\-.]+)""",
    """"vhost":"({web_domain}[\w\-.]+)""",
    """"message":"({additional_info}[^"]+)""",
    """"(http_)?status":"({result_code}[^"]+)""",
    """"http_referrer":"(<n\/a>|({referrer}[^"]+))""",
    """"http_method":"({method}[^"]+)""",
    """"host":"({host}[^"]+)""",
    """"entry_url":"({url}[^"]+)""",
    """"entry_path":"({uri_path}[^"]+)""",
    """"entry_query":"(<n\/a>|({uri_query}[^"]+))""",
    """"client_ip":"({src_ip}[A-Fa-f:\d.]+)""",
    """"req_size":"({bytes_in}\d+)""",
    """"resp_size":"({bytes_out}\d+)""",
  ]


}
```