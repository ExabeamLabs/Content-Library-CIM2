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
    """"timestamp":({time}\d{10})""",
    """"hostname":"({src_host}[^"]+)"""",
    """"userip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"appcategory":"({category}[^"]+)"""",
    """"other_categories":\[({categories}[^\]]+?)\]"""
    """"action":"({action}[^"]+)""",
    """"page":"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)"""",
    """"policy":"({additional_info}[^"]+)"""",
    """"page":"(\w+:\/\/)?({web_domain}[^\\\/"]+)"""",
    """"user":"\s*({email_address}[^\s"@]+?@[^\s"]+\.[^\s"]+)"""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"browser":"(unknown|({browser}[^"]+))"""",
    """"src_location":"({src_location}[^"]+)"""",
    """"src_country":"({src_country}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"referer":"({referrer}[^"]+)""""
    """"file_size":({bytes}\d+)""",
    """"activity":"({operation}[^"]+)""""
  
}
```