#### Parser Content
```Java
{
Name = pan-ngfw-csv-http-session-webbrowsing
   ParserVersion = v1.0.0
   Vendor = Palo Alto Networks
   Product = Palo Alto NGFW
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
   Conditions = [
""",THREAT,url,""",
"""web-browsing,"""
   ]
   Fields = [
    """({event_category}THREAT)""",
    """THREAT,[^,]+,[^,]+,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """THREAT,[^,]+,[^,]+,({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z),""",
    """THREAT,([^,]+,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,({src_translated_ip}[^,]+),({dest_translated_ip}[^,]+)""",
    """,THREAT,([^,]*?,){8}(({email_address}[^@,]+@[^\.]+\.[^,]+)|(({domain}[\w\.\-]{1,40}?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),"""
    """THREAT,url,([^,]*,){21}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),[^,]*,(?:|({protocol}[^,]+)),(?:|({action}[^,]*)),""",
    """THREAT,url,([^,]*,){26}("+)?({url}[^\\\/\s:,"]+({uri_path}\/[^\?\s,"]+)?)"?"""
    """Informational,([^,]*,){11}"+}({user_agent}.+?)\s*"""",
    """THREAT,url,([^,]*,){26}("+)?.*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+)[\\\/\s:"]"""
    """,(any|({category}[^,]+?)),Informational,client to server,"""
   ]
 

}
```