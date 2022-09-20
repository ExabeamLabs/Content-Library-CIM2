#### Parser Content
```Java
{
Name = pingidentity-pi-sk4-app-authentication-success-delivery
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"PINGID"""",""""type":"user"""",""""status":"delivery"""","""destinationServiceName =Ping""",""""resources":""" ]
  Fields = [
    """"recorded":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"actors":\[\{"type":"user","name":"({user}[^"]+?)"""",
    """"status":"({result}delivery)""",
    """"message":"({additional_info}[^}]+?)"\s*\}""",
    """destinationServiceName =({app}Ping)""",
    """subject":"({email_subject}[^:]+?)","\w+":""",
    """"toAddress":"({recipient}[^"]+?)",""",
    """"smtpResponse":"({additional_info}[^"]+?)","""
  ]
  ParserVersion = "v1.0.0"


}
```