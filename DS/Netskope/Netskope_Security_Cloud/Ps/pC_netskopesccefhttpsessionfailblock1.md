#### Parser Content
```Java
{
Name = netskope-sc-cef-http-session-fail-block-1
  ParserVersion = v1.0.0
  Conditions = [
""""alert_type":"policy""""
""""action":"block""""
""""traffic_type":"Web""""
]

cef-netskope-web = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":({time}\d+)""",
    """"hostname":"({src_host}[^"]+)"""",
    """"userip":"({src_ip}[A-Fa-f:\d.]+)"""",
    """"appcategory":"({category}[^"]+)"""",
    """"other_categories":\[({categories}[^\]]+?)\]"""
    """"action":"({action}[^"]+)""",
    """"page":"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)"""",
    """"policy":"({additional_info}[^"]+)"""",
    """"page":"(\w+:\/\/)?({web_domain}[^\\\/"]+)"""",
    """"user":"\s*({email_address}[^\s"@]+?@[^\s"]+\.[^\s"]+)"""",
    """"dstip":"({dest_ip}[A-Fa-f.:\d]+)"""",
    """"browser":"(unknown|({browser}[^"]+))"""",
    """"src_location":"({src_location}[^"]+)"""",
    """"src_country":"({src_country}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"referer":"({referrer}[^"]+)""""
    """"file_size":({bytes}\d+)""",
    """"activity":"({operation}[^"]+)""""
  
}
```