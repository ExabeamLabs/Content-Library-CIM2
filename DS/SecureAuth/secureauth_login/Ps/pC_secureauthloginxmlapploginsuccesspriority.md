#### Parser Content
```Java
{
Name = secureauth-login-xml-app-login-success-priority
Vendor = SecureAuth
Product = SecureAuth Login
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<Priority>""","""Success</Message>""" ]
Fields = [
"""<UserHostAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""<HostName>({host}[^<]+)""",
"""<EventID>({event_code}\d+)</EventID>""",
"""<UserID>({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
"""<Realm>({app}[^<]+)""",
"""<UserAgent>(?:-|({user_agent}[^<]+))""",
]
ParserVersion = v1.0.0


}
```