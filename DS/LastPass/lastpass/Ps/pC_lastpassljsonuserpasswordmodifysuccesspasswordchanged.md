#### Parser Content
```Java
{
Name = lastpass-l-json-user-password-modify-success-passwordchanged
  Vendor = LastPass
  Product = LastPass
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """event-name":"password-changed""", """Action":"Master Password Changed""", """src-application-name":"LastPass Enterprise""", """"is-successful":true""" ]
  Fields = [
    """"time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}Z)"""",
    """\d\d\dZ\s({host}[\w\-.]+)""",
    """"user-email":"({email_address}[^@"]+@[^"\.]+\.[^"]+)"""",
    """"src-ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"application-action":"({operation}[^"]+)""",
    """"event-name":"({event_name}[^"]+)"""",
    """"app-user-displayname":"({full_name}[^"]+)""""
   ]


}
```