#### Parser Content
```Java
{
Name = "bromium-aes-cef-alert-trigger-success-hostrecorded"
Vendor = "Bromium"
Product = "Bromium Secure Platform"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Bromium, Inc.|BEM|"""
"""|Host threat recorded|"""
]
Fields = [
"""\s({host}[\w\-.]+)\sCEF:\d+\|Bromium, Inc.\|"""
"""\|Bromium, Inc.\|([^\|]*\|){3}({alert_name}[^\|]+)"""
"""\|Bromium, Inc.\|([^\|]*\|){4}({alert_severity}\d+)"""
"""(\s|\|)shost=({src_host}[^\s]+)"""
"""(\s|\|)src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\s|\|)suser=({user}[^\s@]+)@?.+?\s(\w+=|$)"""
"""(\s|\|)cs1=({process_path}({process_dir}(?:[^\s]+)?[\\\/]+)?({process_name}[^\\\/]+?))\s+cs1Label=Resources"""
"""(\s|\|)msg=({additional_info}.+?)\s+(\w+=|$)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```