#### Parser Content
```Java
{
Name = "dg-ndlp-kv-alert-trigger-success-endpointusername"
Vendor = Digital Guardian
Product = Digital Guardian Network DLP
TimeFormat = "yyyy/MM/dd H:mm:ss"
Conditions = [
""" [endpoint_user_name=""""
""" [policy_rule=""""
]
Fields = [
"""\w+ \d\d \d\d:\d\d:\d\d ({host}[\w.\-]+) \S+ \["""
"""\s\[computer=\"({src_host}[^\"]+)"""
"""\s\[url=\"(N\/A|({malware_url}[^\"]+))"""
"""\s\[app_name=\"({process_name}[^\"]+)"""
"""\s\[id=\"({alert_id}[^\"]+)"""
"""\s\[endpoint_user_name=\"(({domain}[^\"]+)[\\\/]+)?({user}[^\"\\\/]+)"""
"""\s\[ip_addr=\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\s\[protocol_device_taisyou=\"({alert_type}[^\"]+)"""
"""\s\[policy_rule=\"({alert_name}[^\"]+)"""
"""\s\[syadan=\"({action}[^\"]+)"""
"""\s\[jyudaido=\"({alert_severity}[^":]+)"""
"""\s\[soushinsya=\"(N\/A|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\s\[taisyou_ip=\"(N\/A|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\s\[tenpu_file_name=\"[^\"]*?({malware_file_name}[^\"\\\/]+?)\s*\""""
"""\s\[hasseibi=\"({time}\d\d\d\d\/\d\d\/\d\d \d+:\d+:\d+)"""
]
ParserVersion = "v1.0.0"


}
```