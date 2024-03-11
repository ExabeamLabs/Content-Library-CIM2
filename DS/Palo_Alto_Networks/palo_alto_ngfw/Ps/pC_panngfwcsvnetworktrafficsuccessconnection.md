#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-success-connection
  ParserVersion = v1.0.0 
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
""",THREAT,url,"""
  ]
  Fields = [
    """THREAT,url,[^,]+,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """THREAT,[^,]+,[^,]+,({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z),""",
    """THREAT,url,([^,]+,){2}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,({src_translated_ip}[A-Fa-f\d:.]+),({dest_translated_ip}[A-Fa-f\d:.]+),""",
    """THREAT,url,([^,]*,){26}(\\?"+)?(\w+:\/{2})?(www\.)?({web_domain}[^,\\?:"]+?)[\\\/\s:"]"""
    """THREAT,([^,]*,){7}({rule}[^,]+?)\s*,""",
    """THREAT,([^,]*,){8}(({email_address}[^@,]+@[^,\.]+\.[^,]+)|(({domain}[^,\\]+?)[\\]{1,2})?({user}[^,\\\/]+))"""
    """THREAT,([^,]*,){10}(not-applicable|({network_app}[^,]+?))\s*,""",
    """THREAT,([^,]*,){12}({src_network_zone}[^,]+?)\s*,""",
    """THREAT,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,""",
    """THREAT,([^,]*,){20}({src_port}\d+?)\s*,""",
    """THREAT,([^,]*,){21}({dest_port}\d+?)\s*,""",
    """THREAT,([^,]*,){22}({src_translated_port}\d+?)\s*,""",
    """THREAT,([^,]*,){23}({dest_translated_port}\d+?)\s*,""",
    """THREAT,([^,]*,){25}({protocol}[^,]+?)\s*,""",
    """THREAT,([^,]*,){26}({action}[^,]+?)\s*,""",
    """THREAT,url,([^,]*,){26}(\\?"+)?(\w+:\/{2})?(www\.)?({web_domain}[^\/\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+)[\\\/\s:"]""",
    """,(any|unknown|({category}[^,]+?)),Informational,client to server,"""
    """THREAT,([^,]*,){35}(((\d{1,3}\.){3}\d{1,3})\-((\d{1,3}\.){3}\d{1,3})|({dest_country}[^,]+?))\s*,"""
    ]


}
```