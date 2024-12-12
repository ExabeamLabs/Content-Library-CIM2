#### Parser Content
```Java
{
Name = netskope-sc-cef-http-session-success-cloudapp
 ParserVersion = v1.0.0
 Conditions = [
  """"page":"""
  """"traffic_type":"""
  """"CloudApp""""
  """"url":"""
 ]

cef-netskope-web = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"hostname":\s*"({src_host}[\w\.\-]+)"""",
    """"userip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"appcategory":\s*"(-|none|({categories}({category}[^",;:]+)[^"]*?))"""",
    """"other_categories":\[({categories}[^\]]+?)\]"""
    """"action":\s*"({action}[^"]+)""",
    """"page":\s*"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)"""",
    """"policy":\s*"({additional_info}[^"]+)"""",
    """"page":\s*"(\w+:\/\/)?({web_domain}[^\\\/"]+)""",
    """"user":\s*"\s*({email_address}[^\s"@]+?@[^\s"]+\.[^\s"]+)"""",
    """"dstip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"browser":\s*"(unknown|({browser}[^"]+))"""",
    """"src_location":\s*"({src_location}[^"]+)"""",
    """"src_country":\s*"({src_country}[^"]+)"""",
    """"os":\s*"({os}[^"]+)"""",
    """"referer":\s*"({referrer}[^"]+)""""
    """"file_size":({bytes}\d+)""",
    """"activity":\s*"({operation}[^"]+)""""
    """"protocol":\s*"({protocol}[^"]+)""""
    """"access_method":\s*"({auth_method}[^"]+)""""
    """"domain":\s*"({web_domain}[^"]+)""""
    """"client_bytes":({bytes_in}\d+)"""
    """"server_bytes":({bytes_out}\d+)"""
    """"app":\s*"({app}[^,"]+)"""" 
    """"dst_location":\s*"({location}[^"]+)""""
    """"dst_country":\s*"({dest_country}[^"]+)""""
    """"dstport":\s*"({dest_port}\d+)"""
  
}
```