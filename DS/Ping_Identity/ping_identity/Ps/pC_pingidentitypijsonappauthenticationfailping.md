#### Parser Content
```Java
{
Name = "pingidentity-pi-json-app-authentication-fail-ping"
Vendor = "Ping Identity"
Product = "Ping Identity"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""application-msg":"""
"""SSO Auth. Canceled from server"""
""""triggered-by":"""
"""Ping"""
]
Fields = [
"""time"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""+hostname"+:"+({host}[^"]+)"""
"""app-username"+:"+(({email_address}[^@\s"]+@[^"\s]+)|({user}[^"\s]+))"""
""""src-application-name"+:"+({app}[^"]+)"""
""""application-msg"+:"+({failure_reason}[^}\]]+?)\s*"[,\]}]"""
]
ParserVersion = "v1.0.0"


}
```