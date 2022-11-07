#### Parser Content
```Java
{
Name = google-cloudplatform-mix-app-activity-success-prototpayload
  Vendor = Google
  Product = Cloud Platform
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"protoPayload":""", """googleapis.com""", """"resourceName":""" ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[\w\-.]+)\s\d+\s""",
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"callerIp":\s*"({src_ip}[^"]+)""",
    """"callerSuppliedUserAgent":\s*"({user_agent}[^"]+)""",
    """"principalEmail":\s*"(?:({email_address}[^"@]+?@({email_domain}[^"@]+))|({user}[^"]+))"""",
    """"methodName":\s*"({operation}[^"]+)""",
    """"resourceName":\s*"({resource}[^"]+?(\/({object}[^"\/]+))?)"""",
    """"serviceName":\s*"({app}[^"]+)""",
    """\sdproc=({app}[^=]+)\s\w+="""
  ]


}
```