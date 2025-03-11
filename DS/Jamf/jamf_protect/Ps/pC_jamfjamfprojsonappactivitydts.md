#### Parser Content
```Java
{
Name = jamf-jamfpro-json-app-activity-dts
  Vendor = "Jamf"
  Product = "Jamf Protect"
  ExtractionType = json
  TimeFormat = "epoch"
  ParserVersion = "v1.0.0"
  Conditions = [ """"product":"Device Telemetry Stream"""", """"vendor":"Jamf"""" ]
  Fields = [
    """exa_json_path=$.host.hostname,exa_field_name=host"""
    """exa_json_path=$.host.os,exa_field_name=os"""
    """exa_json_path=$.host.provisioningUDID,exa_field_name=udid"""
    """exa_json_path=$.host.serial,exa_field_name=host_key"""
    """exa_json_path=$.host.protectVersion,exa_field_name=app_version"""
    """exa_json_path=$.host.ips[0],exa_field_name=dest_ip"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.metadata.product,exa_field_name=product_name"""
    """exa_json_path=$.metadata.vendor,exa_field_name=vendor_name"""
    """exa_json_path=$.process.ppid,exa_field_name=process_id"""
    """exa_json_path=$.thread.thread_id,exa_field_name=thread_id"""
    """exa_json_path=$.thread.uuid,exa_field_name=user_uid"""
    """exa_json_path=$.action.result..result_type,exa_field_name=response_type"""
    """exa_json_path=$.action.result.result.auth,exa_field_name=result"""
    """exa_json_path=$.event_type,exa_field_name=event_category"""
    """exa_json_path=$.action_type,exa_field_name=operation_type"""
  ]


}
```