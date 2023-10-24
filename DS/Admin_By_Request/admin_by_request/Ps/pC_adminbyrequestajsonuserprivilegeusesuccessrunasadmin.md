#### Parser Content
```Java
{
Name = adminbyrequest-a-json-user-privilege-use-success-runasadmin
  Vendor = Admin By Request
  Product = Admin By Request
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"type":"Run As Admin"""" , """"elevatedApplications":""", """"approvedBy":""", """"traceNo":"""" ]
  Fields = [
    """"requestTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"user":[^=]+?"account":"(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """"user":[^=]+?"email":"({email_address}[^@"]+@[^\."]+\.[^"]+)""",
    """"user":[^=]+?"fullName":"({full_name}[^"]+)""",
    """"computer":[^=]+?"name":"({host}[^"]+)""",
    """"computer":[^=]+?"model":"({additional_info}[^"]+?)"""",
    """"type":"({event_name}Run As Admin)"""",
    """"application":\{[^=]*?"file":"({object}[^"]+)""",
    """"elevatedApplications":\[\{[^=]+?"file":"({object}[^"]+)"""
  ]
  ParserVersion = v1.0.0


}
```