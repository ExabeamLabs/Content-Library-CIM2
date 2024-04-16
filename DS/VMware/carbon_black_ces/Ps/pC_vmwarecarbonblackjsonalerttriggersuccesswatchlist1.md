#### Parser Content
```Java
{
Name = vmware-carbonblack-json-alert-trigger-success-watchlist-1
  Vendor = VMware
  Product = Carbon Black CES
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"legacy_alert_id"""", """"threat_indicators"""", """"device_username":""", """_threat_category"""", """"type":""", """"WATCHLIST"""" ]
  Fields = [
    """exa_json_path=$.create_time,exa_field_name=time"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.threat_id,exa_field_name=threat_id"""
    """exa_json_path=$.device_username,exa_regex=(({email_address}[^@,"]+@[^",]+)|(({domain}[^\\"]+?)\\+)?({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.device_name,exa_regex=(\w+\\+)?({host}[^."]+)"""
    """exa_json_path=$.threat_indicators[:1].process_name,exa_field_name=process_name"""
    """exa_json_path=$.reason,exa_field_name=additional_info"""
    """exa_json_path=$.threat_indicators[:1].sha256,exa_field_name=hash_sha256"""
    """exa_json_path=$.policy_name,exa_field_name=policy_name"""
    """exa_json_path=$.workflow.state,exa_field_name=state"""
    """exa_json_path=$.type,exa_field_name=alert_type"""
    """exa_json_path=$.legacy_alert_id,exa_field_name=alert_id"""
    """exa_json_path=$.org_key,exa_field_name=primary_key"""
    """exa_json_path=$.threat_cause_threat_category,exa_regex=(UNKNOWN|({result}[^"]+?))"""
    """exa_json_path=$.report_name,exa_field_name=alert_name"""
    """exa_json_path=$.report_id,exa_field_name=alert_id"""
    """exa_json_path=$.process_name,exa_field_name=process_name"""
    """exa_json_path=$.threat_cause_actor_name,exa_regex=({process_path}({process_dir}[^"]+)\\({process_name}[^"]+))"""
  ]


}
```