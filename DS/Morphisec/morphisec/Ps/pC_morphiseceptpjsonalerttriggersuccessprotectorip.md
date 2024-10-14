#### Parser Content
```Java
{
Name = "morphisec-eptp-json-alert-trigger-success-protectorip"
Vendor = "Morphisec"
Product = "Morphisec"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""Protector IP":[""""
""""Attack Time":[""""
""""Attacked Module":[""""
]
Fields = [
"""d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d ({host}[\w.\-]+) Morphisec"""
""""Protector IP\":\[\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""Message\":\[\"({additional_info}[^\"]+)\""""
"""({alert_name}attack)"""
""""Logged In UserName\":\[\"(({domain}[^\\\/\"]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
""""Attacked Module\":\[\"({malware_url}[^\"]+)\""""
""""Attack Time\":\[\"({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
""""Computer Name\":\[\"({src_host}[^\"]+)\""""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```