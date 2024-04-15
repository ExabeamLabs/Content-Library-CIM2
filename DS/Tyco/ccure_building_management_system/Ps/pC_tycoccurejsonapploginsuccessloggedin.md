#### Parser Content
```Java
{
Name = "tyco-ccure-json-app-login-success-loggedin"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""messagetype":""""
""""statecode":"LoggedIn""""
""""primaryobjectname":""""
]
Fields = [
""""messageutc":"({time}[^"]+)"""
""""statecode":"({event_name}[^"]+)"""
""""primaryobjectname":"*(null|({last_name}[^",]+?)\s*,\s*({first_name}[^",]+?))\s*""""
"""<ApplicationName[^>]*>({app}[^<"]+)<\/ApplicationName>"""
]
ParserVersion = "v1.0.0"


}
```