#### Parser Content
```Java
{
Name = "watchguard-w-kv-http-session-success-httprequest"
Vendor = "Watchguard"
Product = "Watchguard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""msg="HTTP request""""
"""http-proxy"""
"""dstname=""""
]
Fields = [
"""(({host}[\w.\-]+)\s+)?\(({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\s*\d\d)\)\s+http-proxy"""
"""\s+({protocol}\S+)\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_port}\d+)\s+msg="HTTP request""""
"""\sproxy_act="({proxy_action}[^"]+)""""
"""\sop="({method}[^"]+)""""
"""\sdstname="({web_domain}[^"]+)""""
"""\sarg="({uri_path}[^"\?]+(\?({uri_query}[^"]+))?)""""
"""\ssent_bytes="({bytes_in}\d+)"""
"""\srcvd_bytes="({bytes_out}\d+)"""
"""\sapp_cat_name="({category}[^"]+)""""
"""\ssrc_user="({email_address}[^"]+)""""
]
DupFields = [
"email_address->user"
]
ParserVersion = "v1.0.0"


}
```