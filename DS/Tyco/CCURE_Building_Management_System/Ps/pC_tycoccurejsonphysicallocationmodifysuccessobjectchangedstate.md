#### Parser Content
```Java
{
Name = tyco-ccure-json-physical-location-modify-success-objectchangedstate
  Vendor = Tyco
  Product = CCURE Building Management System
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"messagetype":"ObjectChangedState"""", """"statecode":"""", """"primaryobjectname":"""" ]
  Fields = [
    """"messageutc":"({time}[^"]+)""",
    """"statecode":"({operation}[^"]+)""",
    """"messagetype":"({result}[^"]+)""",
    """"primaryobjectname":"({object}[^"]+)""",
    """"primaryobjecttype":"({object_type}[^"]+)""",
  ]


}
```