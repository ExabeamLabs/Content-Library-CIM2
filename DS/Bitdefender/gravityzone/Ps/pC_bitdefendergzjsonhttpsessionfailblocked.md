#### Parser Content
```Java
{
Name = "bitdefender-gz-json-http-session-fail-blocked"
Vendor = "Bitdefender"
Product = "GravityZone"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""gravityzone:"""
""""status":"uc_site_blocked""""
]
Fields = [
""""last_blocked":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""user":\{[^\}]*?"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""computer_name":"({host}[^"]+)"""
""""url":"({url}({web_domain}[^"\\\/:]+)(:({dest_port}\d+))?({uri_path}[\\\/]+[^"\?]*?)({uri_query}\?[^"]*)?)""""
]
ParserVersion = "v1.0.0"


}
```