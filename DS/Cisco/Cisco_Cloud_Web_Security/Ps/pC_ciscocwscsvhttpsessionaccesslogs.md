#### Parser Content
```Java
{
Name = cisco-cws-csv-http-session-accesslogs
    Vendor = Cisco
    Product = Cisco Cloud Web Security
    TimeFormat = "epoch_sec"
    Conditions = [ """ accesslogs: Info: """ ]
    Fields = [
      """({host}[\w.\-]+)\s+accesslogs:\s+Info:\s+({time}\d+)\.\d+\s+\S+\s+(-|({src_ip}[a-fA-F\d.:]+))\s+(NONE|({proxy_action}[^\s\/]+))\/({http_response_code}\d+)\s+\S+\s+(-|({method}\S+))\s+({url}(({protocol}\w+):\/+)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\s\/]*?([^\.\s]+)))(:({dest_port}\d+))?({uri_path}\/[^\s\?]*?)?({uri_query}\?[^\s]*?)?)((\s+(-|"(({domain}[^"\/\\@]+)[\\\/]+)?({user}[^\\\/@"]+)[^"]*")\s)|\s*$|\s)""",
      """\s<\w+_([^,]*,){22}"\s*({category}[^"]+?)\s*"""",
    ]
	ParserVersion = "v1.0.0"
  

}
```