#### Parser Content
```Java
{
Name = "infoblox-bddi-cef-alert-trigger-success-alert"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Infoblox|"""
""" act="ALERT"""
]
Fields = [
"""CEF:([^\|]*\|){4}({rule_id}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
"""act="({action}[^"]+)"""
"""cat="({operation}[^"]+)"""
"""spt=({src_port}\d+)"""
"""dpt=({dest_port}\d+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""fqdn=(((?i)na\s)|({src_host}[\w\-.]+))"""
"""fqdn=({top_domain}[^\s]+)\s*"""
]
DupFields = ["operation->alert_type"]
ParserVersion = "v1.0.0"


}
```