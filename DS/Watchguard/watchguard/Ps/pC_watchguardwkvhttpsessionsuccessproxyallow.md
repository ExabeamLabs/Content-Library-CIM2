#### Parser Content
```Java
{
Name = "watchguard-w-kv-http-session-success-proxyallow"
Vendor = "Watchguard"
Product = "Watchguard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""ProxyAllow"""
"""msg_id="""
"""proxy_act"""
"""msg="""
]
Fields = [
"""(({host}[\w.\-]+)\s+)?\(({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\s*\d\d)\)\s+http[s]?-proxy"""
"""\s+({protocol}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_port}\d+)\s+msg=""""
"""\sproxy_act="({proxy_action}[^"]+)""""
"""\sop="({method}[^"]+)""""
"""\sarg="(?:\/|({uri_path}[^"]+))""""
"""\sdstname="({url}({web_domain}(?!\*|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[^"]*?([^\s."]+)))""""
"""\ssent_bytes="({bytes_in}\d+)"""
"""\srcvd_bytes="({bytes_out}\d+)"""
"""\scats="({category}[^"]+)""""
"""\ssrc_user="({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)[^"]+)""""
"""action="+({proxy_action}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```