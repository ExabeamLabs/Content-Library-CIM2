#### Parser Content
```Java
{
Name = "bromium-aes-cef-alert-trigger-success-hostthreatfilehash"
Vendor = "Bromium"
Product = "Bromium Secure Platform"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Bromium, Inc.|BEM|"""
"""|Host threat file hash|"""
]
Fields = [
"""\s({host}[\w\-.]+)\sCEF:\d+\|Bromium, Inc.\|"""
"""\|Bromium, Inc.\|([^\|]*\|){3}({alert_name}[^\|]+)"""
"""\|Bromium, Inc.\|([^\|]*\|){4}({alert_severity}\d+)"""
"""(\s|\|)shost=({src_host}[^\s]+)"""
"""(\s|\|)src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\s|\|)suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@?.+?\s(\w+=|$)"""
"""(\s|\|)fname=({malware_url}.+?)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}.+?)\s{0,100}(\w+=|$)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```