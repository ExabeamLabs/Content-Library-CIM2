#### Parser Content
```Java
{
Name = zeek-z-json-email-send-receive-rcptto
  ParserVersion = v1.0.0
  Conditions = [ 
"""id.orig_h"""
"""id.resp_h"""
"""mailfrom"""
"""rcptto"""
]
  Fields = ${ZeekParsersTemplates.json-bro-activity.Fields}[
    """"helo":\s*"({helo}[^"]+)""",
    """"mailfrom":\s*"({email_address}[^"@]+@([^"@]+))""",
    """"rcptto":\[({email_recipients}"({dest_email_address}[^",@]+@([^"@,]+))".*?)\]""",
    """"subject":\s*"({email_subject}[^"]+)""",
    """"user_agent":\s*"({user_agent}[^"]+)"""
  ]

json-bro-activity = {
  Vendor = Zeek
  Product = zeek
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """"ts\\?"+:[\[\\]*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """"uid\\?"+:\\?"+({connection_id}[^"]+)""",
    """"id\.orig_h\\?"+:\\?"+({src_ip}[a-fA-F\d.:]+)""",
    """"id\.orig_p\\?"+:({src_port}\d+)""",
    """"id\.resp_h\\?"+:\\?"+({dest_ip}[a-fA-F\d.:]+)""",
    """"id\.resp_p\\?"+:({dest_port}\d+)""",
    """"proto\\?"+:\\?"+({protocol}[^"]+)"""
  
}
```