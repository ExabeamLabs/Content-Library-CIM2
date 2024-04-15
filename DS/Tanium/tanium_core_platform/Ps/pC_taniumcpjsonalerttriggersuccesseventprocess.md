#### Parser Content
```Java
{
Name = "tanium-cp-json-alert-trigger-success-eventprocess"
Vendor = "Tanium"
Product = "Tanium Core Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""trace_process_table_id"""
"""Timestamp"""
"""Computer Name"""
"""Computer IP"""
]
Fields = [
""""Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)""""
""""User Name":"({user}[^"]+?)""""
""""User Id":"({user}[^"]+?)""""
""""User Domain":"({domain}[^"]+?)""""
""""user\\":\\"(({domain}[^"\\]+)\\+)?({user}[^"]+?)\\*""""
""""Priority":"({alert_severity}[^"]+)""""
""""Event Name":"({alert_name}[^"]+)""""
""""Event Name":"({alert_type}[^"]+)""""
""""Event Id":"({alert_id}[^"]+)""""
""""Computer Name":"({src_host}[^"]+?)""""
""""Computer IP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""fullpath\\":\\"({malware_url}[^"]+?)\\*""""
""""name\\":\\"({file_name}[^"]+?)\\*""""
""""md5\\":\\"({hash_md5}[^"]+?)\\*""""
""""payload=\{({additional_info}.+?[^\\]")\}"""
]
ParserVersion = "v1.0.0"


}
```