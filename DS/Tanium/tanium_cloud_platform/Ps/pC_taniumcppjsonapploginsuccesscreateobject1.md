#### Parser Content
```Java
{
Name = tanium-cpp-json-app-login-success-createobject-1
  Conditions = [ """"type_name":"CreateObject"""", """"object_type_name":"authentication"""", """"object_name":"""", """"audit_name":"""", """"details":"""" ]
  Fields = ${TaniumParserTemplates.tanium-cloud-app-events.Fields}[
    """exa_json_path=$.details,exa_field_name=additional_info"""
    """exa_json_path=$.object_type_name,exa_field_name=object_type"""
    """exa_json_path=$.details,exa_regex=UserID:\s*({user_id}[^;]+)"""
    """exa_regex=IP Address\s*:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = v1.0.0

tanium-cloud-app-events = {
  Vendor = Tanium
  Product = Tanium Cloud Platform
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  ExtractionType = json
  Fields = [
    """exa_json_path=$.creation_time,exa_field_name=time"""
    """exa_json_path=$.type_name,exa_field_name=operation"""
    """exa_json_path=$.details,exa_regex=User:\s(System User|({email_address}[^"@;]+@[^";\.]+\.[^";]+)|({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.details,exa_regex=[^"]*?Session ID:\s({session_id}\d+)"""
    """exa_regex="domain":"(<\[)?({domain}[^>\]"]+)(\]>)?"""
    """exa_json_path=$.audit_type,exa_field_name=audit_type"""
  ]
  DupFields = [ "operation->event_name" 
}
```