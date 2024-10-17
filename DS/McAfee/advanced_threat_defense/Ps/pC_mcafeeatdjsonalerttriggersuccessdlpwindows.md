#### Parser Content
```Java
{
Name = mcafee-atd-json-alert-trigger-success-dlpwindows
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = Advanced Threat Defense
  TimeFormat = ["MMM dd, yyyy hh:mm:ss a","MMMM dd, yyyy hh:mm:ss a"]
  Conditions = ["""occurred_endpoint""" , """device_class_name""" , """DLP for Windows"""]
  Fields = [
    """exa_json_path=$.occurred_endpoint,exa_field_name=time""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.incident_type,exa_field_name=alert_type""",
    """exa_json_path=$.computer_ip,exa_field_name=src_ip""",
    """exa_json_path=$.computer_name,exa_field_name=host""",
    """exa_json_path=$.device_friendly_name_,exa_field_name=device_id""",
    """exa_json_path=$.actual_action,exa_field_name=result""",
    """exa_json_path=$.total_content_size_kb,exa_field_name=bytes""",
    """exa_regex="total_content_size_({bytes_unit}[^"]+)":"\d""",
    """exa_json_path=$.user_name,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.user_groups,exa_field_name=additional_info""",
    """exa_json_path=$.incident_id,exa_field_name=alert_id""",
    """exa_json_path=$.destination,exa_field_name=target""",
    """exa_json_path=$.rules,exa_field_name=alert_name""",
    """exa_json_path=$.source_application_file_name,exa_regex=^(?:None|({process_path}[^"]+))""",
    """exa_json_path=$.evidence_file_path,exa_regex=^(?:None|({file_path}\w+:\\+([^\\"]+\\+)+({file_name}[^"]+)))""",
  ]


}
```