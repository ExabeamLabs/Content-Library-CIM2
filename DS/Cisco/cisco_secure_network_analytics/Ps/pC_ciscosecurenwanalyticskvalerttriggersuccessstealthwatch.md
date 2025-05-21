#### Parser Content
```Java
{
Name = "cisco-securenwanalytics-kv-alert-trigger-success-stealthwatch"
Vendor = "Cisco"
Product = "Cisco Secure Network Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""StealthWatch"""
"""|target_hostname"""
"""|alarm_severity_id"""
"""|alarm_type_description"""
]
Fields = [
"""({host}[\w\-.]+) StealthWatch"""
"""\Wtime(=|\|)({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""\|target_hostname(=|\|)(|({dest_host}[^|]+))\|"""
"""\|alarm_type_description(=|\|)({additional_info}[^|]+)\|"""
"""\|port(=|\|)({dest_port}\d+)"""
"""\|target_ip(=|\|)({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\|target_mac_address(=|\|)({dest_mac}[a-fA-F\d.:]+)"""
"""\|alarm_type_name(=|\|)({alert_name}[^|]+)\|"""
"""\|alarm_category_name(=|\|)({alert_type}[^|]+)(\||\s$)"""
"""\|source_hostname(=|\|)(|({src_host}[^|]+))\|"""
"""\|alarm_severity_id(=|\|)({alert_severity}[^|]+)\|"""
"""\|source_ip(=|\|)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\|source_mac_address(=|\|)({src_mac}[a-fA-F\d.:]+)"""
"""\|source_username(=|\|)(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) details"""
"""\|device_ip(=|\|)({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""\|device_name(=|\|)({host}[^|]+)\|"""
"""\|details(=|\|)(|({activity_details}[^|]+))\|"""
"""\|protocol(=|\|)(|({protocol}[^|\s]+?))\s*\|"""
"""\|alarm_id(=|\|)({alert_id}[^|]+)\|"""
]
ParserVersion = "v1.0.0"


}
```