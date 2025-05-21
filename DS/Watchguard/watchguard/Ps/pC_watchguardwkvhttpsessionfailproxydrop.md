#### Parser Content
```Java
{
Name = "watchguard-w-kv-http-session-fail-proxydrop"
Vendor = "Watchguard"
Product = "Watchguard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""msg="ProxyDrop"""
"""https-proxy"""
]
Fields = [
"""(({host}[\w.\-]+)\s+)?\(({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\s*\d\d)\)\s+https-proxy"""
"""\s+({protocol}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_port}\d+)\s+msg="ProxyDrop"""
"""\sproxy_act="({proxy_action}[^"]+)""""
"""\sop="({method}[^"]+)""""
"""\sdstname="({web_domain}[^"]+)""""
"""\sarg="({uri_path}[^"\?]+(\?({uri_query}[^"]+))?)""""
"""\ssent_bytes="({bytes_in}\d+)"""
"""\srcvd_bytes="({bytes_out}\d+)"""
"""\scats="({category}[^"]+)""""
"""\ssrc_user="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""msg="+({proxy_action}Proxy[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```