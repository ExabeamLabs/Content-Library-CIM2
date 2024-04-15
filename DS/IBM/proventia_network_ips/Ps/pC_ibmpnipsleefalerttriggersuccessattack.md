#### Parser Content
```Java
{
Name = "ibm-pnips-leef-alert-trigger-success-attack"
Vendor = "IBM"
Product = "Proventia Network IPS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LEEF:"""
"""|IBM|NIPS|"""
"""cat=Attack"""
]
Fields = [
"""devTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""LEEF:([^\|]*\|){4}({alert_name}[^\|]+)"""
"""cat=({alert_type}[^=\|\#]+)"""
"""proto=({protocol}[^\=\|\#]+)"""
"""sev=({alert_severity}[^\=\|\#]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""srcPort=({src_port}\d+)"""
"""dstPort=({dest_port}\d+)"""
"""status=({action}[^\=\|\#]+)"""
]
ParserVersion = "v1.0.0"


}
```