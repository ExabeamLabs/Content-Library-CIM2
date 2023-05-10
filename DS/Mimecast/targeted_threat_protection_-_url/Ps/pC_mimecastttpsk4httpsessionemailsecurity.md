#### Parser Content
```Java
{
Name = mimecast-ttp-sk4-http-session-emailsecurity
  Vendor = Mimecast
  Product = Targeted Threat Protection - URL
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""destinationServiceName =Mimecast Email Security""", """"action":"""", """"url":"""", """"category":""","""dproc=""" ]
  Fields = [
    """"date":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
    """"userEmailAddress":"({email_address}[^\s@"]+@[^\s@"]+)""",
    """"action":"({action}[^"]+)""",
    """"category":"(Unknown|({category}[^"]+))""",
    """"url":"(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?[\\\/]*(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\\\/\s:,"]+))(:({dest_port}\d+))?({uri_path}\/[^\?",]*?)?({uri_query}\?[^"]*?)?))\s*"""",
  ]
  ParserVersion = "v1.0.0"


}
```