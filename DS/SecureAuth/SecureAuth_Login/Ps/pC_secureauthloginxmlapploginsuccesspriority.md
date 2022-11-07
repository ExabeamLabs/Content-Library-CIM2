#### Parser Content
```Java
{
Name = secureauth-login-xml-app-login-success-priority
    Vendor = SecureAuth
    Product = SecureAuth Login
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """<Priority>""","""Success</Message>""" ]
    Fields = [
	"""<UserHostAddress>({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
	"""<HostName>({host}[^<]+)""",
	"""<EventID>({event_code}\d+)</EventID>""",
	"""<UserID>({user}[^<]+)""",
	"""<Realm>({app}[^<]+)""",
     	"""<UserAgent>(?:-|({user_agent}[^<]+))""",
    ]
	ParserVersion = v1.0.0
  

}
```