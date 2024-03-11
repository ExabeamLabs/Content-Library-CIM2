#### Parser Content
```Java
{
Name = pan-ngfw-csv-http-session-9999
   ParserVersion = v1.0.0
   Vendor = Palo Alto Networks
   Product = Palo Alto NGFW
   TimeFormat = "yyyy/MM/dd HH:mm:ss"
   Conditions = [
""",THREAT,url,""",
"""(9999)"""
   ]
   Fields = [
    """({host}[^\s]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,THREAT,url,""",
    """:\d\d:\d\d\s+({host}[\w.-]+)\s""",
    """THREAT,url,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,""",
    """THREAT,url,([^,]*,){5,8}(({domain}[^\\,]+)\\+)?(|({user}[^,]+)),""",
    """THREAT,url,([^,]*,){4}((\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3},(\d{1,3}\.\d{1,3}.\d{1,3}.\d{1,3},)))?[^,]+,(|x-fwd-for: [^,]+|(({domain}[^\\,]+)\\+)?({user}[^,]+)),""",
    """THREAT,url,([^,]*,){19}(|({src_port}\d+)),(|({dest_port}\d+)),([^,]*,){3}(|({protocol}[^,]+)),(|({action}[^,]*)),""",
    """THREAT,url,.+?"+(?:\\|({url}(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\\\/\s:,"]+))(:({dest_port}\d+))?({uri_path}\/[^\?\s]*?)?(\/|({uri_query}\?[^\s]*?))?))\\?"*,(9999)?\(9999\),""",
    """\(9999\),([^,]*,){8}"?({mime}[^,"]+)""",
    """\(9999\),([^,]*,){8}((".+?")|([^,]*)),([^,]*,){4}"*({user_agent}[^,]+),""",
    """\(9999\),([^,]*,){8}((".+?")|([^,]*)),([^,]*,){4}"+({user_agent}[^"]+?)\s*",""",
    """\(9999\),([^,]*,){16}(|"?({referrer}[^,"\s]+?)"?)\s*,""",
    """,(?i)({method}connect|get|head|post|put|delete|trace|options),"""
    """THREAT,url,([^,]*,){26}(\\?"+)?(\w+:\/{2})?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+)[\\\/\s:"]""",
    """\(9999\),(("[^"]+?"|[^,]*),){36}(N/A|unknown|({threat_category}[^,]+)),""",
    """\(9999\),({category}[^,]+),"""
    """\(9999\),([^,]*,){42}"\s*({categories}({category}[^,"]+)[^"]*?)\s*",""",
    """THREAT,url,([^,]*,){6}({rule}[^,]+)""",
    """THREAT,url,([^,]*,){9}({network_app}[^,]+),""",
    """THREAT,url,([^,]*,){11}({src_network_zone}[^,]+),""",
    """THREAT,url,([^,]*,){12}({dest_network_zone}[^,]+),""",
    """THREAT,url,([^,]*,){13}({src_interface}[^,]+),""",
    """THREAT,url,([^,]*,){14}({dest_interface}[^,]+),""",
    """\(9999\),[^,]*,({severity}[^,]+),""",
    """THREAT,url,([^,]*,){17}({session_id}\d+),""",
    """THREAT,url,([^,]*,){54}({src_host}[\w.-]+)"""
   ]
 

}
```