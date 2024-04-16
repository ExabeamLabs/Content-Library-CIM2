#### Parser Content
```Java
{
Name = lastpass-l-json-app-login-fail-failedloginattempt
  Vendor = LastPass
  Product = LastPass
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"Data":""", """Action":"Failed Login Attempt""","""login-type":"""]
  Fields = [
    """Time":"({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})""",
    """\d\d\dZ\s({host}[\w\-.]+)""",
    """Username":"({email_address}[^@"]+@[^"\.]+\.[^"]+)""",
    """"src-ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"src-application-name"+:"+({app}[^"]+)""",
    """app-user-displayname":"({full_name}[^"]+)""",
    """"application-action":"({operation}[^"]+)""",
    """event-name":"({event_name}[^"]+)"""
   ]


}
```