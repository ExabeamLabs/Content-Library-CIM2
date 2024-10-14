#### Parser Content
```Java
{
Name = "sangfor-ngaf-kv-http-session-websitebrowsing"
Vendor = "Sangfor"
Product = "Sangfor NGAF"
TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
Conditions = [
"""type: website browsing"""
"""<Identifier>ZC01_NTTDHK-FWL-002</Identifier>"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[\+\-]\d+:\d+)\s+\S+\s+fwlog:"""
"""<Identifier>ZC01_({host}[\w\-.]+)<\/Identifier>"""
"""user:\s*\((null|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)"""
"""policy name:\s*({policy_name}[^,"]+)"""
"""Src IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Dst IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""application:\s*({categories}({category}[^;,"]+)[^,]*)"""
"""action:\s*({action}[^,"]+)"""
"""URL:\s*(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)(:({dest_port}\d+))?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s]*)?))""""
]
ParserVersion = "v1.0.0"


}
```