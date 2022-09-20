#### Parser Content
```Java
{
Name = bitglass-casb-json-email-send-success-emailsend
  ParserVersion = v1.0.0
  Vendor = Bitglass
  Product = Bitglass CASB
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """Email, Send, Web""", """ api.bitglass.com """, """"application":""", """"Office 365"""" ]
  Fields = [
    """"time":\s*"({time}\d+ \w+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """"instancename":\s*"({host}[^"]+)"""",
    """"user":\s*"({user}[^"]+)"""",
    """"email":\s*"({email_user}[^"]+)"""",
    """"device":\s*"({os}[^"]+)"""",
    """"application":\s*"({app}[^"]+)"""",
    """"ipaddress":\s*"({src_ip}[a-fA-F\d.:]+)"""",
    """"filename":\s*"({file_name}[^"]+(\.({file_ext}[^."]+))?)",""",
    """"useragent":\s*"({user_agent}.+?)",""",
    """"emailfrom":\s*"({email_address}[^"]+)"""",
    """"emailto":\s*"({email_recipients}[^"]+)"""",
    """"emailto":\s*"({dest_email_address}[^",]+)""",
    """"emailto":\s*"({external_address}[^",@]+@[^",]+)""",
    """"emailsubject":\s*"({email_subject}[^"]+)""""
  ]


}
```