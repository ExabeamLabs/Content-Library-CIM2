#### Parser Content
```Java
{
Name = "stealthbits-s-leef-user-disable-success-accountdisabled"
Vendor = "StealthBits"
Product = "StealthIntercept"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LEEF:1.0|STEALTHbits|"""
"""cat=Account disabled"""
"""AttrOldValue="""
"""Success=True"""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) LEEF"""
"""devTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""usrName =(({domain}[^\\]+)\\)?(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+?))\s+\w+="""
"""AffectedObject=(({dest_domain}[^\\]+)\\)?({dest_user}.+?)\s+\w+="""
"""OrigServer=([^\\]+\\)?({dest_host}.+?)\s+\w+="""
]
DupFields = [
"dest_host->host"
]
ParserVersion = "v1.0.0"


}
```