#### Parser Content
```Java
{
Name = "secureworks-isensor-kv-alert-trigger-success-useragentdetected"
Vendor = "SecureWorks"
Product = "Managed iSensor IPS"
TimeFormat = "epoch_sec"
Conditions = [
"""iSensor: [**]"""
]
Fields = [
"""({host}[\w\.-]+)\s+iSensor:"""
"""\[Time:\s+({time}\d{10})"""
"""iSensor:\s+(\[.*?\]\s+){2}(?:\d+\s+)?(?:VID\d+\s+)?({alert_name}[^\[]+?)\s+\["""
"""\[Event ID:\s+({alert_id}\d+)"""
"""\[Priority:\s+({alert_severity}\d+)"""
"""\[src IP:\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\[dst IP:\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\[EX HTTP_URI 9:\s+({target_uri}.+?)\]\s"""
"""\[EX HTTP_HOSTNAME 10:\s+({target_host}[^\s\]]+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```