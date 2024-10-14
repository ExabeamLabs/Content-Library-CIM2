#### Parser Content
```Java
{
Name = "forcepoint-wsg-kv-http-session-webactivity"
Vendor = "Forcepoint"
Product = "Websense Security Gateway"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss", "MM/dd/yyyy HH:mm:ss"]
Conditions = [
"""category="""
"""bytes_out="""
"""bytes_in="""
"""http_method="""
]
Fields = [
"""({time}\w+ \d+ \d+:\d+:\d+)\s+"""
"""({time}\d\d/\d\d/\d\d\d\d \d\d:\d\d:\d\d)"""
"""({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+(\w+=|$)"""
"""\Wcategory="?({category}.+?)"?,?\s*(\w+=|$)"""
"""\Wsrc_host="?(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-.]+))"""
"""\Wde?st="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Whost_masked="?({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\Wdest_ip_masked="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdst_ip="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wbytes_out="?({bytes_in}\d+)"""
"""\Wbytes_in="?({bytes_out}\d+)"""
"""\Whttp_method="?({method}.+?)"?,?\s*(\w+=|$)"""
"""\Wstatus="?({http_response_code}\d+)"""
"""\Whttp_proxy_status_code="?({http_response_code}\d+)"""
"""\Whttp_server_status_code="?({http_response_code}\d+)"""
"""\Wdisposition="?({action}.+?)"?,?\s*(\w+=|$)"""
"""\Waction="?(?:-|({action}.+?))"?,?\s*(\w+=|$)"""
"""\Wurl="?({url}.+?)"?,?\s+(\w+=|$)"""
"""\Wurl="?(?:-|({protocol}\w+))\\*:\/+"""
"""\Wurl="?(?:-|(\w+\\*:\/+)?[^\/"=]+)({uri_path}\/[^\/][^?\s"]*)"""
"""\Wurl="?[^\?\s"=]*({uri_query}\?[^\s"]*)"?,?(\s+\w+=|\s*$)"""
"""\Wurl="?(?:[^:]+\\*:\/+)?({web_domain}[^\/:\s"]+)"""
"""\Wcache="*({proxy_action}.+?)"*,?\s*(\w+=|$)"""
"""\WReferer="*({referrer}.+?)"*,?\s*(\w+=|$)"""
"""\Whttp_content_type="?(?:-|({mime}.+?))"?,?\s*(\w+=|$)"""
"""\Whttp_user_agent="*({user_agent}[^"]+?)(\s"|")"""
"""\Wuser="?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"?,?\s*(\w+=|$)"""
"""\Wuser="?LDAP.+?DC\\*=org\/({user}[\w\.\-\!\#\^\~]{1,40}\$?)"?,?\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```