#### Parser Content
```Java
{
Name = tanium-cpp-json-app-login-success-createobject
  Conditions = [ """"type_name":"CreateObject"""", """"audit_type":"authentication_audit"""", """"object_name":"""", """"audit_type":"""", """"details":"""" ]
  ParserVersion = v1.0.0

tanium-cloud-app-events = {
  Vendor = Tanium
  Product = Tanium Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"creation_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"type_name":"({operation}[^"]+)"""",
    """"details":"User:\s(System User|({email_address}[^"@;]+@[^";\.]+\.[^";]+)|({user}[\w\.\-]{1,40}\$?))""",
    """"details":"[^"]*?Session ID:\s({session_id}\d+)""",
    """"domain":"(<\[)?({domain}[^>\]"]+)(\]>)?"""",
    """"audit_type":"({audit_type}[^"]+)""""
  ]
  DupFields = [ "operation->event_name" 
}
```