#### Parser Content
```Java
{
Name = "netskope-sc-cef-http-session-success-page"
Conditions = [
""""type":"page""""
""""traffic_type":"Web""""
""""activity":"Browse""""
]
ParserVersion = "v1.0.0"

cef-netskope-alert.Fields}[
    """"time":"({time}[^"]+)""""
    """"srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"alert_type":"({alert_type}[^"]+)""",
    """"action":"({result}[^"]+)""",
    """"hostname":"({src_host}[\w.-]+)"""",
    """"referer":"({referrer}[^"]+)""",
    """"policy":"({additional_info}[^"]+)""",
    """"page":"({web_domain}[^\\\/"]+)""",
    """"severity":({alert_severity}[^,"]+)""",
    """"_id":"({alert_id}[^"]+)""",
    """"file_path":"({file_path_at}[^"]+)"""",
    """"site":"({site_at}[^"]+)""""
  ]
  ParserVersion = v1.0.0
}

{
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "epoch_sec"
Fields = [
""""timestamp":({time}\d{10})"""
""""hostname":"({src_host}[^"]+)"""
""""userip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""appcategory":"({category}[^"]+)"""
""""other_categories":\[({categories}[^\]]+?)\]"""
""""action":"({action}[^"]+)"""
""""page":"({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?)""""
""""policy":"({additional_info}[^"]+)"""
""""page":"(\w+:\/\/)?({web_domain}[^\\\/"]+)"""
""""user":"\s*({email_address}[^\s"@]+?@[^\s"]+\.[^\s"]+)""""
""""dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""browser":"(unknown|({browser}[^"]+))"""
""""src_location":"({src_location}[^"]+)"""
""""src_country":"({src_country}[^"]+)"""
""""os":"({os}[^"]+)"""
""""referer":"({referrer}[^"]+)"""
""""file_size":({bytes}\d+)""",
""""activity":"({operation}[^"]+)""""
]
Name = "netskope-sc-cef-http-session-success-page"
Conditions = [
""""type":"page""""
""""traffic_type":"Web""""
""""activity":"Browse""""
]
ParserVersion = "v1.0.0"
},

{
  Name = netskope-sc-json-network-traffic-traffictype
  ParserVersion = "v1.0.0"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Conditions = [
""""bypass_traffic":"""
""""traffic_type":"""
""""userkey":"""
""""url":"""
]
  Fields = [
    """\"+bypass_reason\"+:\s*\"+({action}[^\",]+)""",
    """"page":"(|({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))"""",
    """"domain":"({web_domain}[^"]+)""""
    """\"+url\"+:\s*\"+(|({web_domain}[^\",\/]+))"""",
    """\"user\"+:\s*\"+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)))"""",
    """\"+dstport\"+:\s*({dest_port}\d+)""",
    """\"hostname\"+:\s*\"+({host}[^\",]+)""",
    """\"+appcategory\"+:\s*\"+({category}[^\",]+)""",
    """\"timestamp\"+:\s*({time}\d{10})""",
    """\"+src_location\"+:\s*\"+({location_city}[^\",]+)""",
    """\"+bypass_traffic\"+:\s*\"+({result}[^\",]+)""",
    """\"+userip\"+:\s*\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\"+src_country\"+:\s*\"+({country_code}[^\",]+)""",
    """\"srcip\":\s*\"({src_translated_ip}[A-Fa-f:\d.]+)\"""",
    """\"+dstip\"+:\s*\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"policy":\s*"({alert_name}[^",]+)""",
    """\"+browser\"+:\s*\"+({browser}[^\",]+)""",
    """\"+useragent\"+:\s*\"+({user_agent}[^\"]*?)","""
    """"protocol":\s*"({protocol}[^"]+)"""",
    """"src_location":"({src_location}[^"]+)"""",
    """"src_country":"({src_country}[^"]+)"""",
    """"dst_location":"({location}[^"]+)"""",
    """"dst_country":"({dest_country}[^"]+)"""",
    """"access_method":\s*"({auth_method}[^"]+)"""",
    """"policy":"({additional_info}[^"]+)"""",
    """"app":"({app}[^,"]+)"""",
    """"appcategory":"(-|none|({categories}({category}[^",;:]+)[^"]*?))"""",
    """"other_categories":\[({categories}[^\]]+?)\]"""
    """"client_bytes":({bytes_in}\d+)"""
    """"server_bytes":({bytes_out}\d+)"""

  
}
```