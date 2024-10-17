#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-leef-alert-trigger-success-lowenforcement"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
Conditions = [
"""LEEF:"""
"""|VMware_Carbon_Black|App_Control|"""
"""srcHostName ="""
"""policy="""
"""dstHostName ="""
"""fileThreat="""
"""fileTrust="""
"""fileId="""
]
Fields = [
"""devTime=({time}\w{1,3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\.\d{1,3}\s\w{1,3})"""
"""\d\d:\d\d:\d\d\s({host}[^\s]+)\sLEEF"""
"""\|App_Control\|[^\|]+\|({alert_name}[^\|]+)"""
"""\Wcat=({alert_type}[^=]+?)\s+\w+="""
"""sev=({alert_severity}\d+)"""
"""externalId=({alert_id}[^=]+?)\s+\w+="""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""srcHostName =(({domain}[^\\\s]+)\\+)?({src_host}[^\s]+)"""
"""srcProcess=({process_path}({process_dir}[^=]*?[\\\/]+)?({process_name}[^\\\/=]+?))\s+\w+="""
"""usrName =(({domain}[^\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""fileName =({file_name}[^=]+?(\.({file_ext}[^=.]+?)?))\s+\w+="""
"""filePath=({file_path}({file_dir}[^=]+?)[^=\\]+?)\s+\w+="""
"""dstHostName =({dest_host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```