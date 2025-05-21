#### Parser Content
```Java
{
Name = "f5-silverline-json-alert-trigger-success-waf"
Product = "F5 Silverline"
Vendor = "F5"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""" type=waf"""
"""attack_type="""
"""x_forwarded_for_header_value="""
"""policy_apply_date="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+({host}\S+)\s+"""
"""attack_type="({alert_type}[^"]+)""""
"""dest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""dest_port="({dest_port}\d+)""""
"""ip_client="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""src_port="({src_port}\d+)"""
"""policy_name="({policy_name}[^"]+)""""
"""protocol="({protocol}[^"]+)""""
"""request_status="({result}[^"]+)""""
""""support_id="({alert_id}[^"]+)"""
"""severity="({alert_severity}[^"]+)""""
"""http_class_name="({domain}[^"]+)""""
"""support_id="({alert_id}[^"]+)""""
"""uri="({uri_path}[^"]+)""""
"""username="(N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""sub_violations="(({additional_info}[^"]+))""""
"""violations="({alert_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```