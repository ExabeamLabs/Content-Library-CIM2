#### Parser Content
```Java
{
Name = "fireeye-nshelix-json-alert-trigger-success-rule"
Vendor = "FireEye"
Product = "FireEye Helix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""type":"fireeye_rule""""
""""threat_type":"""
""""category":"Host""""
]
Fields = [
""""created_at":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""""
""""iocnames":"({alert_name}[^"]+)""""
""""description":"({additional_info}[^"]+)""""
"""virus.+?"description":"({alert_name}[^"]+)""""
""""severity":"({alert_severity}[^"]+)""""
""""threat_type":({alert_type}\d+)"""
""""source":"({dest_host}[^"]+)""""
""""destination":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""details.+?"username":"([\w\s]+\\+)?(system|({user}[\w\.\-]{1,40}\$?))""""
""""process":"({process_name}[^"]+)""""
""""args":"({process_path}.*)","pid""""
""""virus":"({malware_name}[^"]+)""""
""""result":"({result}[^"]+)""""
""""filepath":"({file_path}({file_dir}.*?)({file_name}[^\\\."]+(\.({file_ext}[^\\\."]+))?))""""
""""file_name":"({file_path}({file_dir}.*?)({file_name}[^\\\."]+(\.({file_ext}[^\\\."]+))?))""""
""""file_name":"({file_name}[^\\\."]+(\.({file_ext}[^\\\."]+))?)""""
]
ParserVersion = "v1.0.0"


}
```