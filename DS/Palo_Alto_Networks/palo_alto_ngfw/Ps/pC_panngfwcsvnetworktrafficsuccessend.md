#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-success-end
    ParserVersion = v1.0.0
    Conditions = [
""",TRAFFIC,""",
""",allow,"""
    ]
    Fields = ${PaloAltoParsersTemplates.paloalto-firewall.Fields}[
    """TRAFFIC,([^,]*,){10}({action}(incomplete|insufficient-data))\s*"""
    ]

paloalto-firewall = {
   Vendor = Palo Alto Networks
   Product = Palo Alto NGFW
   TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
   start_timeFormat = ["yyyy/MM/dd HH:mm:ss"]
   Fields = [
     #removed slow regexes for host
     #"""\s({host}[\w\-.]+)\s+(\[.*?\]\s+)?\d+,([^,]*,){2}TRAFFIC,""",
     #""":\d\d:\d\d(([+-]\d\d:\d\d)|(\.\d+Z))?\s+({host}[\w.-]+)\s""",
     """({event_category}TRAFFIC)""",
     """TRAFFIC,({subtype}[^,]+),""",
     """,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),""",
     """TRAFFIC,([^,]*,){2}({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
     """TRAFFIC,([^,]*,){2}({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)""",
     """TRAFFIC,([^,]*,){3}(0.0.0.0|({src_ip}(?!::)((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
     """TRAFFIC,([^,]*,){4}(0.0.0.0|({dest_ip}(?!::)((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
     """TRAFFIC,([^,]*,){5}(0.0.0.0|({src_translated_ip}(?!::)((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
     """TRAFFIC,([^,]*,){6}(0.0.0.0|({dest_translated_ip}(?!::)((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
     """TRAFFIC,([^,]*,){7}({rule}[^,]+?)\s*,""",
     """TRAFFIC,([^,]*,){8}\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?:({domain}({src_domain}[^\s,\\]+))\\)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))),""",
     """TRAFFIC,([^,]*,){9}\s*(?:({dest_domain}[^\s,\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[^\s,]+)),""",
     """TRAFFIC,([^,]*,){10}(not-applicable|({network_app}[^,]+?))\s*,""",
     """TRAFFIC,([^,]*,){12}({src_network_zone}[^,]+?)\s*,""",
     """TRAFFIC,([^,]*,){13}({dest_network_zone}[^,]+?)\s*,""",
     """TRAFFIC,([^,]*,){20}(0|({src_port}\d+)),""",
     """TRAFFIC,([^,]*,){21}(0|({dest_port}\d+)),""",
     """TRAFFIC,([^,]*,){22}(0|({src_translated_port}\d+)),""",
     """TRAFFIC,([^,]*,){23}(0|({dest_translated_port}\d+)),""",
     """TRAFFIC,([^,]*,){25}({protocol}[^,]+?)\s*,""",
     """TRAFFIC,([^,]*,){26}({action}[^,]+?)\s*,""",
     """TRAFFIC,([^,]*,){27}({bytes}\d+)""",
     """TRAFFIC,([^,]*,){28}({bytes_out}\d+)""",
     """TRAFFIC,([^,]*,){29}({bytes_in}\d+)""",
     """TRAFFIC,([^,]*,){31}({start_time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),""",
     """TRAFFIC,([^,]*,){33}(any|unknown|({category}[^,]+?)\s*,)""",
     """TRAFFIC,([^,]*,){37}({src_country}[^\.:\d,]+?)\s*,""",
     """TRAFFIC,([^,]*,){38}({dest_country}[^\.:\d,]+?)\s*,""",
     """TRAFFIC,([^,]*,){18}({session_id}\d+),""",
     """,((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+)),"""
     """TRAFFIC,([^,]*,){14}({src_interface}[^,]+),""",
     """TRAFFIC,([^,]*,){15}({dest_interface}[^,]+),""",
     """TRAFFIC,([^,]*,){42}({result_reason}[^,]+),""",
     """({serial_num}[^,]+),TRAFFIC,""",
     """TRAFFIC,([^,]*,){48}({device_name}({host}[\w.-]+))""",
     """TRAFFIC,([^,]*,){11}({virtual_station_name}[^,\s]+?)\s*,"""
   
}
```