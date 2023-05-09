#### Parser Content
```Java
{
Name = pingidentity-pi-sk4-app-authentication-success-queue
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"PINGID"""",""""type":"user"""",""""status":"queue"""","""destinationServiceName =Ping""",""""resources":""" ]
  Fields = [
    """"recorded":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"actors":\[\{"type":"user","name":"({user}[^"]+?)"""",
    """"status":"({result}queue)""",
    """"message":"({additional_info}[^}]+?)"\s*\}""",
    """destinationServiceName =({app}Ping)""",
    """subject":"({email_subject}[^:]+?)","\w+":""",
    """"fromAddress":"({src_email_address}[^"]+?)",""",
    """"toAddress":"({dest_email_address}[^"]+?)","""
  ]
  ParserVersion = "v1.0.0"


}
```