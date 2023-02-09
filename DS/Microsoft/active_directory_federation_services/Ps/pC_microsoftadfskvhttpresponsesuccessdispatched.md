#### Parser Content
```Java
{
Name = microsoft-adfs-kv-http-response-success-dispatched
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """ Status Code:""", """An HTTP response was dispatched.""", """ audit 510 """, """Response Details:""" ]
  Fields = [
    """Date And Time:\s*({time}\d+-\d+-\d+\s\d+:\d+:\d+)""",
    """({event_code}510)""",
    """Status Code:\s*({dns_response_code}\d+)""",
    """({event_name}An HTTP response was dispatched)""",
  ]
  ParserVersion = "v1.0.0"


}
```