#### Parser Content
```Java
{
Name = "ibm-guardium-kv-alert-trigger-success-guardiumalert"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""GUARDIUM_ALERT"""
]
Fields = [
"""session-start-time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""sessionStart="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
"""\w+ \d{1,2} \d{1,2}:\d{1,2}:\d{1,2}\s*({host}[\w\.-]+)"""
"""rule-desc=({alert_name}[^\^]+)(\^+|$)"""
"""category=({alert_type}[^\^]+)(\^+|$)"""
"""severity=({alert_severity}[^\^]+)(\^+|$)"""
"""sql=({additional_info}[^\^"]+?)(\^+|"|$)"""
"""client-hostname=([^\\]+\\)?({src_host}[\w\-\.]+)(\^+|$)"""
"""client-ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""server-ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""service-name=({service_name}[^\^]+)(\^+|$)"""
"""server-type=({server_group}[^\^]+)(\^+|$)"""
"""src-program=({process_path}({process_dir}(?:[^\^]+)?[\\\/]+)?({process_name}[^\\\/\^]+))(\^+|$)"""
"""db-user=([^\\\^]+\\)?({account}({db_user}[^\^]+))(\^+|$)"""
"""os-user=([^\\\^]+\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\^\^"""
]
ParserVersion = "v1.0.0"


}
```