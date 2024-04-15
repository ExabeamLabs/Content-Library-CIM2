#### Parser Content
```Java
{
Name = "suricata-s-json-alert-trigger-success-pdsuricata"
Vendor = "Suricata"
Product = "Suricata"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""pdsuricata"""
"""suricata"""
"""event_type"""
]
Fields = [
""""+timestamp"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""+event_type"+:\s*"+({alert_type}[^"]+)"+"""
""""+src_ip"+:\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"+"""
""""+src_port"+:\s*({src_port}\d+)"""
""""+dest_ip"+:\s*"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"+"""
""""+dest_port"+:\s*({dest_port}\d+)"""
""""+proto"+:\s*"+({protocol}[^"]+)"+"""
""""+app_proto"+:\s*"+({app_protocol}[^"]+)"+"""
""""+bytes_toserver"+:\s*({bytes_in}\d+)"""
""""+bytes_toclient"+:\s*({bytes_out}\d+)"""
""""+state"+:\s*"+({result}[^"]+)"+"""
""""+reason"+:\s*"+({failure_reason}[^"]+)"+"""
""""+http_user_agent"+:\s*"+({user_agent}[^"]+)"+"""
""""+http_method"+:\s*"+({method}[^"]+)"+"""
""""+filename"+:\s*"+({file_name}[^"]+)"+"""
""""+status"+:\s*"+({event_code}[^,"]+)"""
""""+url"+:\s*"+({uri_path}[^"]+)"+"""
""""+hostname"+:\s*"+({host}[^"]+)"+"""
""""+http_content_type"+:\s*"+({mime}[^"]+)"+"""
"""\s({alert_name}suricata)"""
""""+category"+:\s*"+({category}[^"]+)"""
""""+severity"+:\s*({alert_severity}\d+)"""
""""+signature"+:\s*"+({signature}[^"]+)"""
""""+signature_id"+:\s*({signature_id}\d+)"""
""""+action"+:\s*"+({action}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```