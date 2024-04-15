#### Parser Content
```Java
{
Name = "suricata-ids-json-alert-trigger-success-signature"
Vendor = "Suricata"
Product = "Suricata"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""flow_id"""
"""event_type"""
"""community_id"""
"""action"""
"""signature"""
"""category"""
]
Fields = [
""""timestamp\\?":\\?"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+\+\d+)"""
""""src_ip\\?":\\?"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""src_port\\?":\\?({src_port}\d+)"""
""""dest_ip\\?":\\?"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""dest_port\\?":\\?({dest_port}\d+)"""
""""proto\\?":\\?"({protocol}[^""\\]+)"""
""""flow_id\\?":\\?({alert_id}\d+)"""
""""severity\\?":\\?({alert_severity}\d+)"""
""""+signature\\"+:\s*\\"+({rule_name}[^\\"]+)\\""""
""""+signature_id\\"+:\s*\\({rule_id}\d+)"""
""""+action\\"+:\s*"+\\({action}[^\\"]+)"""
""""host":\{"name":"({host}[^"]+)"""
""""+category\\"+:\s*\\"+({alert_type}[^\\"]+)\\"+"""
""""payload_printable\\":\\"({payload_printable}[^,]+)\\","""
"""msg:\\+"*({alert_name}[^"\\]+)"""
""""+category"+:\s*"+({category}[^"]+)"""
""""app_proto\\":\\"({app_protocol}[^\\"]+)"""
""""rule\\":\\"({rule}[^,\("\\]+?)\s*(\(|"|\\)"""
]
ParserVersion = "v1.0.0"


}
```