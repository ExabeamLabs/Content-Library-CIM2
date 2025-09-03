#### Parser Content
```Java
{
Name = netskope-sc-json-endpoint-activity-success-access_method
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"access_method": "Endpoint"""", """"activity_type":""", """"alert_name":""", """"policy_action": "block"""" , """"alert": "no""""]
  Fields = [
    """exa_json_path=$.access_method,exa_field_name=access_type"""
    """exa_json_path=$.activity_type,exa_field_name=operation_type"""
    """exa_json_path=$.alert_name,exa_field_name=alert_name"""
    """exa_json_path=$.alert_type,exa_field_name=alert_type"""
    """exa_json_path=$.computer_name,exa_field_name=host"""
    """exa_json_path=$.device_type,exa_field_name=device_type"""
    """exa_json_path=$.os,exa_field_name=os"""
    """exa_json_path=$.os_user_name,exa_field_name=os_admin"""
    """exa_json_path=$.policy_action,exa_field_name=action"""
    """exa_json_path=$.policy_name,exa_field_name=policy_name"""
    """exa_json_path=$.process_path,exa_regex=({process_path}({process_dir}[^"]*[\\\/]+)({process_name}[^\\\/"]+?))("|$)"""
    """exa_json_path=$.process_name,exa_field_name=process_name"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.record_type,exa_field_name=record_type"""
    """exa_json_path=$.file_type,exa_field_name=file_type"""
    """exa_json_path=$.activity,exa_field_name=operation"""
    """exa_json_path=$.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.dlp_rule,exa_field_name=rule"""
  ]
  ParserVersion = "v1.0.0"


}
```