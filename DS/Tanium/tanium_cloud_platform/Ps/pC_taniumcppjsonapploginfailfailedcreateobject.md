#### Parser Content
```Java
{
Name = tanium-cpp-json-app-login-fail-failedcreateobject
  Conditions = [ """"type_name":"FailedCreateObject"""", """"audit_type":"authentication_audit"""", """"object_name":"""", """"audit_type":"""", """"details":"""" ]
  Fields = ${TaniumParserTemplates.tanium-cloud-app-events.Fields}[
    """"details":"({additional_info}({failure_reason}[^"\.]+)[^"]+)""""
  ]
  ParserVersion = v1.0.0

tanium-cloud-app-events = {
  Vendor = Tanium
  Product = Tanium Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"creation_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """"type_name":"({operation}[^"]+)"""",
    """"details":"User:\s(System User|({email_address}[^"@;]+@[^";\.]+\.[^";]+)|({user}[^;"]+))""",
    """"details":"[^"]*?Session ID:\s({session_id}\d+)""",
    """"domain":"(<\[)?({domain}[^>\]"]+)(\]>)?"""",
    """"audit_type":"({audit_type}[^"]+)""""
  ]
  DupFields = [ "operation->event_name" 
}
```