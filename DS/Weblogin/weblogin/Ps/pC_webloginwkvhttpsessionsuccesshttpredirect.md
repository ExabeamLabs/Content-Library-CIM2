#### Parser Content
```Java
{
Name = "weblogin-w-kv-http-session-success-httpredirect"
Product = "Weblogin"
Vendor = "Weblogin"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""status=REDIRECT"""
"""sub=http"""
"""uniq="""
"""realm="""
"""authref="""
]
Fields = [
""":\d+\s({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}).*?user=(\s|({user}[^\s]+))\s*ip=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\sstatus=({action}[^\s]+)\s*sub=(\s|({url}({protocol}http|https):({uri_path}\/[^\s\?\"]*)?({uri_query}\?[^\"\s]*)?)|({sub_status}.*?)\suniq).*?authref=({request_cookie}[^\s]+)\s*wl_authref=({private_cookie}[^\s]+)\s*realm=(\s|({web_domain}[^\s]+))"""
]
ParserVersion = "v1.0.0"


}
```