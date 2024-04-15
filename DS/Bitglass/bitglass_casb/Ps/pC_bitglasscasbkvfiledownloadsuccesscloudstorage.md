#### Parser Content
```Java
{
Name = "bitglass-casb-kv-file-download-success-cloudstorage"
Vendor = "Bitglass"
Product = "Bitglass CASB"
TimeFormat = "dd MMM yyyy HH:mm:ss"
Conditions = [
"""api.bitglass.com """
""""Cloudstorage, Downloaded""""
"""email="""
"""ipaddress="""
]
Fields = [
"""time=({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
"""user=({full_name}[^,]+)"""
"""email=({email_address}[^@\s,]+@[^\s,]+)"""
"""application=({app}[^,]+)"""
"""ipaddress=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""activity="({event_name}[^"]+)"""
"""filename=({file_name}[^,]+\.({file_ext}[^.,]+))"""
"""details=({additional_info}[^",]+)"""
"""usergroup="({user_group_name}[^"]+)"""
"""device=({os}[^",]+)"""
"""useragent=({user_agent}[^",]+)"""
]
ParserVersion = "v1.0.0"


}
```