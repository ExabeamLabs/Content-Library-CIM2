#### Parser Content
```Java
{
Name = "netskope-sc-json-file-auditlogevent"
  Vendor = "Netskope"
  Product = "Netskope Security Cloud"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"type":""", """"admin_audit_logs"""", """"audit_log_event":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.audit_log_event,exa_field_name=operation"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_regex=({app}netskope)"""
    """exa_json_path=$.organization_unit,exa_field_name=user_ou"""
    """exa_json_path=$.severity_level,exa_field_name=severity"""
    """exa_json_path=$.supporting_data,exa_field_name=additional_info"""
    """exa_json_path=$.type,exa_field_name=operation_type"""
    """exa_json_path=$.details,exa_field_name=additional_info"""    
  ]
  DupFields = [ "operation->access" ]
  ParserVersion = "v1.0.0"


}
```