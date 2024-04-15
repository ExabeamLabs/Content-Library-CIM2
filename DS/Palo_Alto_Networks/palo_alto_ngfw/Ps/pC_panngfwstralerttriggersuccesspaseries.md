#### Parser Content
```Java
{
Name = "pan-ngfw-str-alert-trigger-success-paseries"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""A device has stopped emitting events"""
"""'PaSeries @"""
]
Fields = [
"""'PaSeries @ ({src_host}[^\s']+)( \(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\))?'"""
"""({alert_name}A device has stopped emitting events)"""
]
ParserVersion = "v1.0.0"


}
```