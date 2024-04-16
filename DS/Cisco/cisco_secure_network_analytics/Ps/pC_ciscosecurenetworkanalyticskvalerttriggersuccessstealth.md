#### Parser Content
```Java
{
Name = "cisco-securenetworkanalytics-kv-alert-trigger-success-stealth"
Vendor = "Cisco"
Product = "Cisco Secure Network Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""" stealth-smc StealthWatch["""
"""protocol=""""
]
Fields = [
"""alarm_time="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\w)"""
"""id="({alert_id}[^"]+)""""
"""sig="({alert_type}[^"]+)""""
"""sev="({alert_severity}[^"]+)""""
"""details="({additional_info}[^"]+)""""
"""src="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""src_name="({src_host}[^"]+)""""
"""dest="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dest_name="({dest_host}[^"]+)""""
"""dest_user="({user}[\w\.\-]{1,40}\$?)""""
"""src_user="({user}[\w\.\-]{1,40}\$?)""""
"""dest_user="({account}[^"]+)""""
"""protocol="({protocol}[^"]+)""""
"""dvc_ip="({host}[a-fA-F\d.:]+)"""
"""dvc="({host}[^"]+)""""
"""domain="({domain}[^"]+)""""
"""port="({dest_port}\d+)""""
]
DupFields = [
"alert_type->alert_name"
]
ParserVersion = "v1.0.0"


}
```