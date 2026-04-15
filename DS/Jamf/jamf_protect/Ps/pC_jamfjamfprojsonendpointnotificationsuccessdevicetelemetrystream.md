#### Parser Content
```Java
{
Name = jamf-jamfpro-json-endpoint-notification-success-devicetelemetrystream
  Vendor = "Jamf"
  Product = "Jamf Protect"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"EventProduct": "Device Telemetry Stream"""", """"EventVendor": "Jamf"""", """"EventSchemaVersion":""" ]
  Fields = [
    """exa_json_path=$.DvcHostname,exa_field_name=host""",
    """exa_json_path=$.TargetHostname,exa_field_name=dest_host""",
    """exa_json_path=$.DvcOs,exa_field_name=os""",
    """exa_json_path=$.DvcSerial,exa_field_name=host_key""",
    """exa_json_path=$.DvcIpAddr[0],exa_field_name=dest_ip""",
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_json_path=$.EventProduct,exa_field_name=product_name""",
    """exa_json_path=$.EventVendor,exa_field_name=vendor_name""",
    """exa_json_path=$.process.ppid,exa_field_name=process_id""",
    """exa_json_path=$.thread.thread_id,exa_field_name=thread_id""",
    """exa_json_path=$.thread.uuid,exa_field_name=log_uid""",
    """exa_json_path=$.action.result.result_type,exa_field_name=response_type""",
    """exa_json_path=$.action.result.result.auth,exa_field_name=result""",
    """exa_json_path=$.EventOriginalType,exa_field_name=event_category""",
    """exa_json_path=$.EventSeverity,exa_field_name=severity"""
    """exa_json_path=$.event.exec.cwd.path,exa_field_name=current_working_dir""",
    """exa_json_path=$.event.exec.dyld_exec_path,exa_regex=({process_path}({process_dir}[^"]+[\/]+)?({process_name}[^"]+))""",
    """exa_json_path=$.process.parent_audit_token.exec_path,exa_field_name=parent_process_path"""
    """exa_json_path=$.event.exec.args,exa_field_name=process_command_line"""
  ]
  ParserVersion = "v1.0.0"


}
```