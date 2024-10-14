#### Parser Content
```Java
{
Name = pingidentity-pi-sk4-app-authentication-success-queue
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"PINGID"""",""""type":"user"""",""""status":"queue"""",""""resources":""" ]
  Fields = [
    """"recorded":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """"actors":\[\{"type":"user","name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"status":"({result}queue)""",
    """"message":"({additional_info}[^}]+?)"\s*\}""",
    """destinationServiceName =({app}Ping)""",
    """subject":"({email_subject}[^:]+?)","\w+":""",
    """"fromAddress":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))",""",
    """"toAddress":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))","""
  ]
  ParserVersion = "v1.0.0"


}
```