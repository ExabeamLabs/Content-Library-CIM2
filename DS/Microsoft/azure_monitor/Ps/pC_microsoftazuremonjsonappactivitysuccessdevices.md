#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-devices
  ParserVersion = v1.0.0
  Conditions = [ """"tenantId":""", """"category":"Devices"""", """"operationName":"Devices"""" ]

microsoft-azuremon-json-events = {
  Vendor = Microsoft
  Product = Azure Monitor
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Fields = [
    """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
    """exa_json_path=$.operationName,exa_field_name=operation"""
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.resultType,exa_field_name=result"""
    """exa_json_path=$.properties.DeviceId,exa_field_name=device_id"""
    """exa_json_path=$.properties.UserEmail,exa_regex=(-|system|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.properties.UPN,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$.properties.OS,exa_field_name=os"""
    """exa_json_path=$.properties.DeviceOperatingSystem,exa_field_name=os"""
    """exa_json_path=$.properties.UserDisplayName,exa_field_name=full_name"""
    """exa_json_path=$.properties.UserName,exa_field_name=user"""
    """exa_json_path=$.properties.DeviceHealthThreatLevel,exa_field_name=threat_level"""
    """exa_json_path=$.properties.SerialNumber,exa_field_name=device_id"""
    """exa_json_path=$.properties.IntuneAccountId,exa_field_name=user_id"""
    """exa_json_path=$.properties.UserId,exa_field_name=user_id"""
    """exa_json_path=$.properties.DeviceName,exa_field_name=host"""
    """exa_json_path=$.properties.DeviceHostName,exa_field_name=host"""
    """exa_json_path=$.properties.Status,exa_field_name=status_msg"""
    """exa_json_path=$.properties.EnrollmentTypeMessage,exa_field_name=additional_info"""
    """exa_json_path=$.properties.ScenarioName,exa_field_name=additional_info"""
    """exa_json_path=$.properties.Description,exa_field_name=additional_info"""
    """exa_json_path=$.properties.EventId,exa_field_name=event_code"""
    """exa_json_path=$.properties.FailureReason,exa_field_name=failure_reason"""
    """exa_json_path=$.properties.MessageId,exa_field_name=message_id"""
    """exa_json_path=$.properties.AlertType,exa_field_name=alert_type"""
    """exa_json_path=$.properties.AlertDisplayName,exa_field_name=alert_name"""
    """exa_json_path=$.properties.UPNSuffix,exa_field_name=domain"""
  ]
  DupFields = [ "operation->event_name" 
}
```