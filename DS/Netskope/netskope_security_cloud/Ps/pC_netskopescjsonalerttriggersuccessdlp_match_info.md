#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-dlp_match_info
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"dlp_action":""", """"file_path":""", """"acting_user":""", """"dlp_match_info"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.file_path,exa_regex=({file_path}({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s"]+))?))("|$)"""
    """exa_json_path=$.file_type,exa_field_name=file_type"""
    """exa_json_path=$.activity,exa_field_name=operation"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.status,exa_field_name=alert_status"""
    """exa_json_path=$.dlp_incident_id,exa_field_name=alert_id"""
    """exa_json_path=$..dlp_policy,exa_field_name=alert_name"""
    """exa_json_path=$..dlp_rules[0].dlp_rule_name,exa_field_name=rule"""
    """exa_json_path=$..dlp_action,exa_field_name=action"""    
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "alert_name"->"alert_type" ]  


}
```