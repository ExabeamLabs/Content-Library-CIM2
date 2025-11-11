#### Parser Content
```Java
{
Name = "f5-ipintelligence-kv-alert-trigger-success-ipi"
Vendor = "F5"
Product = "F5 IP Intelligence"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
""" type = ipi,"""
""",attack_type = """
""",ip_intelligence_threat_name = """
""",ip_intelligence_policy_name = """
]
Fields = [
"""date_time\s*=\s*({time}\w+\s+\d+\s+\d+\s+\d\d:\d\d:\d\d)"""
"""ip_intelligence_policy_name\s*=\s*(|({alert_type}({alert_name}[^,]+))),"""
"""ip_intelligence_threat_name\s*=\s*(|({alert_type}({alert_name}[^,]+))),"""
"""source_ip\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""ip_protocol\s*=\s*({protocol}[^,]+)"""
"""severity\s*=\s*({alert_severity}[^,]+)"""
"""source_port\s*=\s*({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```