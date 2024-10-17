#### Parser Content
```Java
{
Name = mcafee-nsp-json-alert-trigger-success-threatsource
  ExtractionType = json
  Vendor = McAfee
  Product = McAfee Network Security Platform
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""threat_source_ip_address""" , """McAfee Host Intrusion Prevention"""]
  Fields = [
    """exa_json_path=$.event_generated_time,exa_regex=^({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """exa_json_path=$.action_taken,exa_field_name=result""",
    """exa_json_path=$.detecting_product_ipv4_address,exa_field_name=host""",
    """exa_json_path=$.detecting_product_host_name,exa_field_name=host""",
    """exa_json_path=$.threat_source_ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.threat_target_ip_address,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.threat_source_user_name,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({domain}[^\\]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.threat_severity,exa_field_name=alert_severity""",
    """exa_json_path=$.threat_source_process_name,exa_regex=({process_path}\w+:\\+([^\\"]+\\+)+({process_name}[^"]+))""",
    """exa_json_path=$.signature_name_host_ips,exa_field_name=alert_name""",
    """exa_json_path=$.event_description,exa_field_name=alert_type""",
    """exa_json_path=$.threat_source_host_name,exa_field_name=src_host""",
    """exa_json_path=$.event_category,exa_field_name=alert_type""",
    """exa_json_path=$.threat_target_host_name,exa_field_name=dest_host""",
    """exa_json_path=$.threat_type,exa_field_name=additional_info""",
  ]
  ParserVersion = "v1.0.0"


}
```