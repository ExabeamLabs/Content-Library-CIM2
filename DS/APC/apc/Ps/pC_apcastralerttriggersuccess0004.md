#### Parser Content
```Java
{
Name = "apc-a-str-alert-trigger-success-0004"
Vendor = "APC"
Product = "APC"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Detected an unauthorized user attempting"""
""" from """
""" 0x0004"""
]
Fields = [
"""(<\d+>)?(\w+\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w.\-]+)\s+(System:\s*)?({alert_name}Detected an ({alert_type}unauthorized user) attempting to access .*? from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\.?\s+"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```