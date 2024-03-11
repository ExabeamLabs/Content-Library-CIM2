#### Parser Content
```Java
{
Name = adminbyrequest-a-json-user-privilege-use-success-adminsession
  Vendor = Admin By Request
  Product = Admin By Request
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"type":"Admin Session"""" , """"elevatedApplications":""", """"approvedBy":""", """"traceNo":"""" ]
  Fields = [
    """"requestTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"user":[^=]+?"account":"(({domain}[^\\]+)\\+)?({user}[^"]+)""",
    """"user":[^=]+?"email":"({email_address}[^@"]+@[^\."]+\.[^"]+)""",
    """"user":[^=]+?"fullName":"({full_name}[^"]+)""",
    """"computer":[^=]+?"name":"({host}[^"]+)""",
    """"computer":[^=]+?"model":"({additional_info}[^"]+?)"""",
    """"type":"({event_name}Admin Session)"""" 
  ]
  ParserVersion = v1.0.0


}
```