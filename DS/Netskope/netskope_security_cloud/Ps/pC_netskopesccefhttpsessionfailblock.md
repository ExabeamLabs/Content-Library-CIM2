#### Parser Content
```Java
{
Name = netskope-sc-cef-http-session-fail-block
  ParserVersion = v1.0.0
  Conditions = [
""""alert_type":"policy""""
""""action":"block""""
""""traffic_type":"CloudApp""""
]

cef-netskope-web = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"hostname":"({src_host}[\w\.\-]+)"""",
    """"userip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"appcategory":"(-|none|({categories}({category}[^",;:]+)[^"]*?))"""",
    """"other_categories":\[({categories}[^\]]+?)\]"""
    """"action":"({action}[^"]+)""",
    """"page":"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)"""",
    """"policy":"({additional_info}[^"]+)"""",
    """"page":"(\w+:\/\/)?({web_domain}[^\\\/"]+)""",
    """"user":"\s*({email_address}[^\s"@]+?@[^\s"]+\.[^\s"]+)"""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"browser":"(unknown|({browser}[^"]+))"""",
    """"src_location":"({src_location}[^"]+)"""",
    """"src_country":"({src_country}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"referer":"({referrer}[^"]+)""""
    """"file_size":({bytes}\d+)""",
    """"activity":"({operation}[^"]+)""""
    """"protocol":"({protocol}[^"]+)""""
    """"access_method":\s*"({auth_method}[^"]+)""""
    """"domain":"({web_domain}[^"]+)""""
    """"client_bytes":({bytes_in}\d+)"""
    """"server_bytes":({bytes_out}\d+)"""
    """"app":"({app}[^,"]+)"""" 
    """"dst_location":"({location}[^"]+)""""
    """"dst_country":"({dest_country}[^"]+)""""
    """"dstport":"({dest_port}\d+)"""
  
}
```