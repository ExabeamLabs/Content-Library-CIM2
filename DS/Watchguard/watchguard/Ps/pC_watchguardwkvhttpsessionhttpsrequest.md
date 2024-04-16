#### Parser Content
```Java
{
Name = "watchguard-w-kv-http-session-httpsrequest"
Vendor = "Watchguard"
Product = "Watchguard"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""msg="HTTPS Request""""
"""https-proxy"""
]
Fields = [
"""(({host}[\w.\-]+)\s+)?\(({time}\d\d\d\d-\d\d-\d\dT\d\d:\s*\d\d:\s*\d\d)\)\s+https-proxy"""
"""\s+({protocol}\S+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+({dest_port}\d+)\s+msg="HTTPS Request""""
"""\sproxy_act="({proxy_action}[^"]+)""""
"""\s(cn|sni)="({web_domain}(?!\*|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[^"]*?([^\s."]+))""""
"""\ssent_bytes="({bytes_in}\d+)"""
"""\srcvd_bytes="({bytes_out}\d+)"""
"""\sapp_cat_name="({category}[^"]+)""""
"""\ssrc_user="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
"""action="+({proxy_action}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```