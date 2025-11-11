#### Parser Content
```Java
{
Name = pan-ngfw-csv-http-session-9999
   Conditions = [
""",THREAT,url,""",
"""(9999)"""
   ]
   Fields = ${PaloAltoParsersTemplates.pan-csv-threat.Fields}[
    """THREAT,url,\d+,[^,]*,([A-Fa-f0-9:.]+,){2,4}[^,]*,(|x-fwd-for: [^,]+|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)),(|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({dest_domain}[^\\,]+)\\+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}([^\s,]+[\s,])+[^,]+)),""",
    """THREAT,url,([^,]*,){19}(|({src_port}\d+)),(|({dest_port}\d+)),([^,]*,){3}(|({protocol}[^,]+)),(|({action}[^,]*)),""",
    """THREAT,url,.+?"+(?:\\|({url}(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|([^\\\/\s:,"]+))(:({dest_port}\d+))?({uri_path}\/[^\?\s]*?)?(\/|({uri_query}\?[^\s]*?))?))\\?"*,(9999)?\(9999\),""",
    """\(9999\),([^,]*,){8}"?({mime}[^,"]+)""",
    """\(9999\),([^,]*,){16}(|"?({referrer}[^,"\s]+?)"?)\s*,""",
    """,({method}connect|get|head|post|put|delete|trace|options),"""
    """\(9999\),(("[^"]+?"|[^,]*),){36}(N/A|unknown|({threat_category}[^,]+)),""",
    """THREAT,url,([^,]*,){26}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))""",
   ]
 
pan-csv-threat = {
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Fields = [
    """,THREAT,([^,]*,){2}({time}[^,]+),"""
    """({event_category}THREAT)"""
    """({serial_num}[^,]+),THREAT,"""
    """,THREAT,({alert_type}({alert_name}[^,]+)),"""
    """,THREAT,([^,]*,){3}({src_ip}(?!::)[a-fA-F\d.:]+)"""
    """,THREAT,([^,]*,){4}({dest_ip}(?!::)[a-fA-F\d.:]+)"""
    """,THREAT,([^,]*,){5}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """,THREAT,([^,]*,){6}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """THREAT,([^,]*,){7}({rule}[^,]+?)\s*,"""
   """,THREAT,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\*)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),"""
    """,THREAT,([^,]*,){9}\s*(({dest_email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({dest_domain}[^\s,\\]+)\\*)?({dest_user}[^\s,]+)),"""
    """,THREAT,([^,]*,){10}({alert_source}({network_app}({app}[^,]+))),""",
    """,THREAT,([^,]*,){11}({virtual_station_name}[^,]+),""",
    """,THREAT,([^,]*,){12}({src_network_zone}[^,]+?)\s*,"""
    """,THREAT,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,"""
    """,THREAT,([^,]*,){14}({src_interface}[^,]+),"""
    """,THREAT,([^,]*,){15}({dest_interface}[^,]+),""",
    """,THREAT,([^,]*,){18}({session_id}\d+),""",
    """,THREAT,([^,]*,){20}({src_port}\d+),"""
    """,THREAT,([^,]*,){21}({dest_port}\d+),"""
    """,THREAT,([^,]*,){22}({src_translated_port}\d+)""",
    """,THREAT,([^,]*,){23}({dest_translated_port}\d+)""",
    """,THREAT,([^,]*,){24}({result_code}[^,]+),""",
    """,THREAT,([^,]*,){25}({protocol}[^,]+?),"""
    """,THREAT,([^,]*,){26}({action}[^,]+?),"""
    """,THREAT,([^,]*,){27}\\?("+)?.*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx))+)[\\\/\s:"]"""
    """,THREAT,([^,]*,){27}([\\"]*(({url}({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?))|({file_name}({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+,))"""
    """,THREAT,([^,]*,){28}(|({alert_name}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,"""
    """,THREAT,([^,]*,){65}({threat_category}[^,]+),"""
    """,((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+)),"""
    """,({threat_id}[^,]+)?,({categories}({category}[^,]+))?,({severity}({alert_severity}(?i)(low|medium|high|critical|informational))),({direction}[^,]+)?,([^,]*,){2}({src_location}[^,]+)?,({dest_country}[^,]+)?,(([^,]*,){35}"+\s*({=categories}({=category}[^,\n"]+)\s*[^"]*)"+,)?"""
  
}
```