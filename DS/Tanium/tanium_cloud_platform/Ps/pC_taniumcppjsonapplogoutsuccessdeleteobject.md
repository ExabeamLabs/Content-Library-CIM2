#### Parser Content
```Java
{
Name = tanium-cpp-json-app-logout-success-deleteobject
  Vendor = Tanium
  Product = Tanium Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"type_name":"DeleteObject"""", """"audit_type":"authentication_audit"""", """"object_name":"""", """"audit_type":"""", """"details":"""" ]
  Fields = [
    """"creation_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"type_name":"({operation}[^"]+)"""",
    """"details":"User:\s(System User|({email_address}[^"@;]+@[^";\.]+\.[^";]+)|({user}[^;"]+))""",
    """"details":"[^"]*?Session ID:\s({session_id}\d+)""",
    """"domain":"(<\[)?({domain}[^>\]"]+)(\]>)?"""",
    """"audit_type":"({audit_type}[^"]+)""""
  ]
  DupFields = [ "activity->event_name" ]
  ParserVersion = v1.0.0


}
```