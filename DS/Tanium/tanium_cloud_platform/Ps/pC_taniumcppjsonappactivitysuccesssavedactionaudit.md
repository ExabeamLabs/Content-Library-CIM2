#### Parser Content
```Java
{
Name = tanium-cpp-json-app-activity-success-savedactionaudit
  Conditions = [ """"type_name":"""", """"audit_type":"saved_action_audit"""", """"object_name":"""", """"audit_type":"""", """"details":"""" ]
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