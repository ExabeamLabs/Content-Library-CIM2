#### Parser Content
```Java
{
Name = secureauth-login-xml-app-activity-catchall-auditeventid
Vendor = SecureAuth
Product = SecureAuth Login
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<Priority>""","""<Category>AUDIT<""", """<Appliance>""", """<Version""" ]
Fields = [
   """<HostName>({host}[^<]+)""",
   """<EventID>({event_id}\d+)</EventID>""",
   """<UserID>({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
   """<Realm>({app}[^<]+)""",
   """<UserAgent>(?:-|({user_agent}[^<]+))""",
   """<Message>({additional_info}[^<]+)"""
   """<Category>({category}[^<]+)"""
   """<UserHostAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   """<UserID>({user_id}[^<]+)<"""
   """<Priority>({priority}\d+)<"""
]
ParserVersion = v1.0.0


}
```