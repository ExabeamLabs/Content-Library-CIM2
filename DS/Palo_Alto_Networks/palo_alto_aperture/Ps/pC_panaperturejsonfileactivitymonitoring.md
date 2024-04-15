#### Parser Content
```Java
{
Name = "pan-aperture-json-file-activitymonitoring"
Vendor = "Palo Alto Networks"
Product = "Palo Alto Aperture"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""cloud_app_instance"""
""""activity_monitoring""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)Z"""
"""\Wuser"?\s*(=|:)\s*"(Unknown|({email_address}[^@"]+@[^"]+))""""
"""\Wcloud_app_instance"?\s*(=|:)\s*"({app}[^"]+)""""
"""\Wsource_ip"?\s*(=|:)\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""\Witem_name"?\s*(=|:)\s*"({file_name}[^"]+?(\.\s*({file_ext}[^\."]+?))?)""""
"""\Waction"?\s*(=|:)\s*"({access}[^"]+)""""
"""\Witem_type"?\s*(=|:)\s*"({file_type}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```