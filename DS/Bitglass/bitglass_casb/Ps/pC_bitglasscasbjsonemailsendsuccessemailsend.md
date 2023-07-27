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
    """"user":\s*"(({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))"""",
    """"email":\s*"({email_user}[^"]+)"""",
    """"device":\s*"({os}[^"]+)"""",
    """"application":\s*"({app}[^"]+)"""",
    """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"filename":\s*"({file_name}[^"]+(\.({file_ext}[^."]+))?)",""",
    """"useragent":\s*"({user_agent}.+?)",""",
    """"emailfrom":\s*"({src_email_address}[^"]+)"""",
    """"emailto":\s*"({email_recipients}[^"]+)"""",
    """"emailto":\s*"({dest_email_address}[^",]+)""",
    """"emailto":\s*"({external_address}[^",@]+@[^",]+)""",
    """"emailsubject":\s*"({email_subject}[^"]+)""""
  ]


}
```