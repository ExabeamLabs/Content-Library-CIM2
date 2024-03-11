#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-success-browsersession
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [""""app":""", """"access_method":""", """"category":""", """"browser_session_id":""", """"src-application-name":"Netskope""""]
  Fields = [
    """"time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}Z)"""",
    """"event-name":"({event_name}[^"]+)"""",
    """"src-ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"app":"({app}[^"]+)""",
    """"domain":"({domain}[^"]+)"""",
    """"user-email":"({email_address}[^@"]+@[^"\.]+\.[^"]+)"""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"useragent":"({user_agent}[^"]+)"""",
    """"type":"({operation}[^",]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```