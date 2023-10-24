#### Parser Content
```Java
{
Name = "mimecast-seg-cef-app-activity-success-messageviewlogs"
Vendor = "Mimecast"
Product = "Mimecast Secure Email Gateway"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """destinationServiceName =Mimecast Email Security"""
  """"viewer":""""
  """"discoveryCase":"""
  """"contentViewed":"""
  """dproc="""
]
Fields = [
  """"viewed":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)""""
  """"viewer":"\s*(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))""""
  """({app}Mimecast Email Security)"""
  """({operation}Archive Message View Logs)"""
  """"subject":"({object}[^"]+?)""""
  """"to":"(({dest_email_address}[^"@]+@[^";]+)|({target}[^"]+)")""",
  """"from":"({log_source}[^"]+?)""""
  """"discoveryCase":({result}\w+)"""
  """"source":"({resource}[^"]+?)""""
  """({additional_info}"contentViewed[^}]+?)\}"""
]
ParserVersion = "v1.0.0"


}
```