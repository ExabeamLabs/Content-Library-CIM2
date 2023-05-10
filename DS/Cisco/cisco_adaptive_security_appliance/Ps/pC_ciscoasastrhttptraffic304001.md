#### Parser Content
```Java
{
Name = cisco-asa-str-http-traffic-304001
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """-304001""", """%ASA-""" ]
  Fields = [
    """Original Address=({host}\S+) ({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d) ({=host}[\w\-.]+).*?ASA-({priority}\d+)-({event_code}\d+): (({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({user}[^\s@]+)@({=src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+?)) ({event_name}.+?) (({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?)):({url}({protocol}[^:]+)\:\/+({web_domain}[^\/:\s"]+)({uri_path}\/[^?\s"]*)?({uri_query}\?[^\s"]+)?)""",
    """({top_domain}(?!(?:\d+\.){3}\d+)[^\.\s\/:]+(?=(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za))+(\s|\/|$))[^\s\/]+)""",
  ]


}
```