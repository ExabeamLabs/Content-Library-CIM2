#### Parser Content
```Java
{
Name = "stealthbits-s-leef-user-enable-success-accountenable"
Vendor = "StealthBits"
Product = "StealthIntercept"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""LEEF:1.0|STEALTHbits|"""
"""cat=Account enabled"""
"""AttrOldValue="""
"""Success=True"""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}[\w\-.]+) LEEF"""
"""devTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""usrName =(({domain}[^\\]+)\\)?({user}.+?)\s+\w+="""
"""AffectedObject=(({dest_domain}[^\\]+)\\)?({dest_user}.+?)\s+\w+="""
"""OrigServer=([^\\]+\\)?({dest_host}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```