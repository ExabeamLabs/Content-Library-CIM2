#### Parser Content
```Java
{
Name = f5-nginx-str-network-traffic-nginxaccess
  Vendor = F5
  Product = NGINX
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
  ParserVersion = v1.0.0
  Conditions = [ """ NGINX_ACCESS """, """" """" ]
  Fields = [
    """\s({host}[\w\-.]+)\s+NGINX_ACCESS""",
    """ NGINX_ACCESS ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """ \[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d{4})\]\s""",
    """\d\d\d\d\]\s"(|({additional_info}[^"]+))"\s({http_response_code}\d+)\s({bytes}\d+)\s""",
    """ NGINX_ACCESS ({url}[^\s]+)\s({protocol}\w+)\/[^"]+"\s({http_response_code}\d+)\s({bytes}\d+)\s"(-|({referrer}[^"]+))"\s"(-|({user_agent}[^"]+))""""
  ]


}
```