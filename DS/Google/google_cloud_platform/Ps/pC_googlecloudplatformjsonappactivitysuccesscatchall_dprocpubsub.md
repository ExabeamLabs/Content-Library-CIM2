#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-activity-success-catchall_dprocpubsub
    Vendor = Google
    Product = Google Cloud Platform
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","epoch","MM.dd.yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
    ParserVersion = "v1.0.0"
    Conditions = [ """destinationServiceName =Google Cloud""", """dproc=Cloud PubSub""",  ]
    Fields = [
    """exa_json_path=$.alert_severity,exa_field_name=alert_severity"""
    """exa_json_path=$.src_host,exa_field_name=src_host"""
    """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d).?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.additional_info,exa_field_name=additional_info"""
    """exa_json_path=$.alert_id,exa_field_name=alert_id"""
    """exa_json_path=$.alert_name,exa_field_name=alert_name"""
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.scan_result,exa_field_name=result"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.time,exa_regex=({time}\d{10})"""
    """exa_json_path=$.severity,exa_field_name=severity"""
    """exa_json_path=$.logName,exa_field_name=log_name"""
    """exa_json_path=$.resource.type,exa_field_name=resource_type""",
    """exa_json_path=$.resource.labels.project_id,exa_field_name=project_id""",
    """exa_json_path=$.resource.labels.zone,exa_field_name=zone""",
    """exa_json_path=$.resource.labels.location,exa_field_name=region""",
    """exa_json_path=$.jsonPayload.message,exa_field_name=additional_info"""
    """exa_json_path=$.reason,exa_field_name=failure_reason"""
    """exa_json_path=$.profileUser,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.userAgent,exa_field_name=user_agent"""
    """exa_json_path=$.url,exa_field_name=url"""
    """exa_json_path=$.event,exa_field_name=event_name"""
    """exa_json_path=$.result,exa_field_name=result"""
  ]


}
```