#### Parser Content
```Java
{
Name = "fireeye-nshelix-json-alert-trigger-success-fireeyerule"
Vendor = "FireEye"
Product = "Network Security (Helix)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""type":"fireeye_rule""""
""""threat_type":"""
""""category":"Network""""
]
Fields = [
""""created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""message":"({alert_name}[^"]+)"""
""""severity":"({alert_severity}[^"]+)"""
""""threat_type":({alert_type}\d+)"""
""""source":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""destination":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""protocol":"({protocol}[^"]+)"""
""""srcdomain":"({additional_info}[^"]+)"""
""""username":"(system_user|({user}[^"]+))"""
""""description":"({policy_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```