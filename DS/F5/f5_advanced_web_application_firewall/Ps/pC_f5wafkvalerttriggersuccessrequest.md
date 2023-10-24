#### Parser Content
```Java
{
Name = "f5-waf-kv-alert-trigger-success-request"
Vendor = "F5"
Product = "F5 Advanced Web Application Firewall"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" perl["""
"""] Request """
""" violations: """
"""HTTP protocol compliance sub violations:"""
]
Fields = [
"""\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+)"""
"""\Wsource ip:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsource port:\s*({src_port}\d+)"""
"""\Wdestination ip:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdestination port:\s*({dest_port}\d+)"""
"""] Request ({result}[^:,]+)"""
"""violations:\s*({alert_name}.+?)\s*HTTP protocol compliance sub violations:"""
"""\Wrequest:\s*<\S+ ({additional_info}\S+)"""
"""\Wviolation_rate:\s*({alert_severity}\d+)"""
"""username:\s*<(N\/A|({user}[\w\.\-]{1,40}\$?))"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```