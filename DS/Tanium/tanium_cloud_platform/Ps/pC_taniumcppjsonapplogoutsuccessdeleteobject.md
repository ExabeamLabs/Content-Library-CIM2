#### Parser Content
```Java
{
Name = tanium-cpp-json-app-logout-success-deleteobject
  ExtractionType = json
  Vendor = Tanium
  Product = Tanium Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"type_name":"DeleteObject"""", """"audit_type":"authentication_audit"""", """"object_name":"""", """"audit_type":"""", """"details":"""" ]
  Fields = [
    """exa_json_path=$.creation_time,exa_field_name=time"""
    """exa_json_path=$.type_name,exa_field_name=operation"""
    """exa_json_path=$.details,exa_regex=User:\s(System User|({email_address}[^"@;]+@[^";\.]+\.[^";]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.details,exa_regex=Session ID:\s({session_id}\d+)"""
    """exa_json_path=$.audit_type,exa_field_name=audit_subcategory"""
  ]
  DupFields = [ "activity->event_name" ]
  ParserVersion = v1.0.0


}
```