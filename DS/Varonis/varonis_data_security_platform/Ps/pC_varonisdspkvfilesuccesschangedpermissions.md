#### Parser Content
```Java
{
Name = "varonis-dsp-kv-file-success-changedpermissions"
Vendor = "Varonis"
Product = "Varonis Data Security Platform"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""Acting Object SAM Account Name:"""
"""Changed Permissions:"""
]
Fields = [
"""Event Time:\s*({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""\sActing Object:\s*({domain}[^\\\s]+)"""
"""\sActing Object SAM Account Name:\s*({user}.+?)\s+File Server"""
"""\sIP Address/Host:\s*(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))|({dest_host}[^\s]+))"""
"""\sEvent Type:\s*({access}.+?)\s*IP Address"""
"""\sAffected Object:\s*({file_name}.+?)\s*Event Type:"""
"""\sAffected Object:\s*.*(?=\.)({file_ext}.+?)\s*Event Type:"""
"""\sPath:\s*({file_path}.+?)\s*Affected Object:"""
"""\sPath:\s*({file_dir}.+?)\\[^\\]+\s+Affected Object:"""
]
DupFields = [
"access->event_code"
]
ParserVersion = "v1.0.0"


}
```