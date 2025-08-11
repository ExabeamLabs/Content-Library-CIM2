#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-data"
Conditions = [
  """,THREAT,data,"""
]
Fields = ${PaloAltoParsersTemplates.pan-csv-threat.Fields}[
  """,THREAT,({alert_type}[^,]+),[^,]*,({time}\d\d\d\d/\d\d/\d\d \d\d:\d\d:\d\d),({src_ip}[\da-fA-F\.:]+),({dest_ip}[\da-fA-F\.:]+)(,|$)"""
  """,THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){27}({device_name}({host}[\w\-\.]+))(,|$)"""
  """,THREAT,data,([^,]*,){8}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(|({domain}[^\\,]+))\\?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(,|$)"""
  """,THREAT,data,([^,]*,){7}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(|({domain}[^\\,]+))\\?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(,|$)"""
  """,THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),({alert_name}[^,]+)(,|$)"""
  """,THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){4}({alert_id}\d+)(,|$)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
    "src_ip->malwareVictimHost"
    "alert_type->malwareCategory"
    "dest_ip->malwareAttackerIp"
    "action->description"
 ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
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
    """,THREAT,([^,]*,){7}({rule}[^,]+?)\s*,"""
    """,THREAT,([^,]*,){8}\s*(({email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({src_domain}[^\s,\\]+)\\*)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))),"""
    """,THREAT,([^,]*,){9}\s*(({dest_email_address}[^@,]+@[^\.]+\.[^,]+)|(?:({dest_domain}[^\s,\\]+)\\*)?({dest_user}[^\s,]+)),"""
    """,THREAT,([^,]*,){10}({network_app}({app}[^,]+?))\s*,""",
    """,THREAT,([^,]*,){11}({virtual_station_name}[^,]+?)\s*,""",
    """,THREAT,([^,]*,){12}({src_network_zone}[^,]+?)\s*,"""
    """,THREAT,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,"""
    """,THREAT,([^,]*,){14}({src_interface}[^,]+),"""
    """,THREAT,([^,]*,){15}({dest_interface}[^,]+),""",
    """,THREAT,([^,]*,){18}({session_id}\d+),""",
    """,THREAT,([^,]*,){20}({src_port}\d+),"""
    """,THREAT,([^,]*,){21}({dest_port}\d+),"""
    """,THREAT,([^,]*,){22}({src_translated_port}\d+)""",
    """,THREAT,([^,]*,){23}({dest_translated_port}\d+)""",
    """,THREAT,([^,]*,){24}({result}[^,]+?),""",
    """,THREAT,([^,]*,){25}({protocol}[^,]+?),"""
    """,THREAT,([^,]*,){26}({action}[^,]+?),"""
    """,THREAT,([^,]*,){27}\\?("+)?.*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx))+)[\\\/\s:"]"""
    """,THREAT,([^,]*,){27}([\\"]*(({url}({malware_url}[^<>".,]+(?:\.[^<>\/\s,]+)?\/[^<>]*?))|({file_name}({malware_file_name}[^<>,]+?)|[^,]*?)[\\\/]*"+,))"""
    """,THREAT,([^,]*,){28}(|({alert_name}[^\(,]+(\(\w+\))?))\s*\(({alert_id}\d+)?""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,"""
    """,THREAT,([^,]*,){65}({threat_category}[^,]+),"""
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """,({threat_id}[^,]+?)?,({categories}({category}[^,]+?))?,({severity}({alert_severity}(?i)(low|medium|high|critical|informational))),({direction}[^,]+?)?,([^,]*,){2}({src_location}[^,]+?)?,({dest_country}[^,]+?)?,(([^,]*,){35}"+\s*({=categories}({=category}[^,\n"]+)\s*[^"]*)"+,)?"""
  
}
```