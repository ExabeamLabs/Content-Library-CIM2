#### Parser Content
```Java
{
Name = tanium-cpp-json-app-login-success-createobject-1
  Conditions = [ """"type_name":"CreateObject"""", """"object_type_name":"authentication"""", """"object_name":"""", """"audit_name":"""", """"details":"""" ]
  Fields = ${TaniumParserTemplates.tanium-cloud-app-events.Fields}[
    """"details":"({additional_info}[^"]+)""""
	  """"details":"[^"]*?IP Address:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	  """"object_type_name":"({object_type}[^"]+)""""
    """UserID:\s*({user_id}[^;]+)"""
  ]
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