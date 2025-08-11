#### Parser Content
```Java
{
Name = netskope-sc-json-network-traffic-traffictype-1
  ParserVersion = "v1.0.0"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  Conditions = [ """"netskope_pop":""", """"traffic_type":""", """"userkey":""", """"appcategory":""", """"ur_normalized":""" ]
  Fields = [
    """"type":\s*"({operation_type}[^"]+)""",
    """"traffic_type":\s*"({app_type}[^"]+)""",
    """"os_family":\s*"({os}[^"]+)""",
    """"os":\s*"({os}[^"]+)""",
    """"ip_protocol":\s*"({protocol}[^"]+)"""",
    """"dsthost":\s*"((({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)|({dest_host}[^"]+))"""",
    """"action":\s*"({action}[^"]+)"""",
    """"transaction_id":\s*"({transaction_id}[^"]+)"""",
    """"useragent":\s*"({user_agent}[^"]+)"""",
    """"browser":\s*"(unknown|({browser}[^"]+))"""",    
    """\"+bypass_reason\"+:\s*\"+({action}[^\",]+)""",
    """"page":"(|({url}(\w+:\/\/)?(({dest_ip}[A-Fa-f.:\d]+)|({web_domain}[^\/]+?))({uri_path}\/[^\?]*?)?({uri_query}\?[^"]+)?))"""",
    """"domain":"({web_domain}[^"]+)""""
    """\"+url\"+:\s*\"+(|({web_domain}[^\",\/]+))"""",
    """"shared_domains":\s*"[\[\<\s]?({domain}[^"\s,\\\]\>]+)""",
    """\"user\"+:\s*\"+(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)))"""",
    """\"+dstport\"+:\s*({dest_port}\d+)""",
    """\"hostname\"+:\s*\"+({host}[^\",]+)""",
    """\"+appcategory\"+:\s*\"+({category}[^\",]+)""",
    """\"timestamp\"+:\s*({time}\d{10})""",
    """\"+src_location\"+:\s*\"+({location_city}[^\",]+)""",
    """\"+bypass_traffic\"+:\s*\"+({result}[^\",]+)""",
    """\"+userip\"+:\s*\"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\"+src_country\"+:\s*\"+({country_code}[^\",]+)""",
    """\"srcip\":\s*\"({src_translated_ip}[A-Fa-f:\d.]+)\"""",
    """\"+dstip\"+:\s*\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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
  ]


}
```