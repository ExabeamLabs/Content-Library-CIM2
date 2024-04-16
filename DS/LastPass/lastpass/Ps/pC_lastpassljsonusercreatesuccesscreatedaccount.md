#### Parser Content
```Java
{
Name = lastpass-l-json-user-create-success-createdaccount
  Vendor = LastPass
  Product = LastPass
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """event-name":"audit-event""", """Action":"Created LastPass Account""", """application-action":"Created LastPass Account""" ]
  Fields = [
    """"time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}Z)"""",
    """\d\d\dZ\s({host}[\w\-.]+)""",
    """"Username":"({email_address}[^@"]+@[^"\.]+\.[^"]+)"""",
    """"src-ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"application-action":"({operation}[^"]+)""",
    """"event-name":"({event_name}[^"]+)""""
   ]


}
```