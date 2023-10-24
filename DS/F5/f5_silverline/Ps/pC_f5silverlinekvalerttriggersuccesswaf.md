#### Parser Content
```Java
{
Name = "f5-silverline-kv-alert-trigger-success-waf"
Vendor = "F5"
Product = "F5 Silverline"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" type = waf,"""
""", policy_name="""
""", request_status="""
""", violations="""
]
Fields = [
"""date_time=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""dest_ip\s*=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dest_port\s*=\s*({dest_port}\d+)"""
"""policy_name\s*=\s*(|({policy_name}[^,]+)),"""
"""attack_type\s*=\s*({alert_type}[^,]+)"""
"""attack_type\s*=\s*({alert_name}[^,]+)"""
"""violations\s*=\s*(|({alert_name}[^,]+)),"""
"""ip_client\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""protocol\s*=\s*({protocol}[^,]+)"""
"""request_status\s*=\s*({result}[^,]+)"""
"""severity\s*=\s*({alert_severity}[^,]+)"""
"""src_port\s*=\s*({src_port}\d+)"""
"""username\s*=\s*(N\/A|({user}[\w\.\-]{1,40}\$?)),"""
]
ParserVersion = "v1.0.0"


}
```