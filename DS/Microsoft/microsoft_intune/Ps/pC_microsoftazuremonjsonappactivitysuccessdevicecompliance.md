#### Parser Content
```Java
{
Name = microsoft-azuremon-json-app-activity-success-devicecompliance
  Product = Microsoft Intune
  ParserVersion = v1.0.0
  Conditions = [ """"tenantId":""", """"category":"DeviceComplianceOrg"""", """"operationName":""", """"IntuneAccountId":""" ]

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
    """exa_json_path=$.resultType,exa_field_name=result,exa_match_expr=!Contains($.resultType,"None")"""
    """exa_json_path=$..DeviceId,exa_field_name=device_id"""
    """exa_json_path=$..UserEmail,exa_regex=(-|system|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$..UPN,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_json_path=$..OS,exa_field_name=os"""
    """exa_json_path=$..DeviceOperatingSystem,exa_field_name=os"""
    """exa_json_path=$..UserDisplayName,exa_field_name=full_name"""
    """exa_json_path=$..UserName,exa_regex=(-|({full_name}[^"\s]+\s[^"]+)(\s*\(\w+\))?|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$..DeviceHealthThreatLevel,exa_field_name=threat_level"""
    """exa_json_path=$..SerialNumber,exa_field_name=device_id"""
    """exa_json_path=$..IntuneAccountId,exa_field_name=user_id"""
    """exa_json_path=$..UserId,exa_field_name=user_id"""
    """exa_json_path=$..DeviceName,exa_field_name=host"""
    """exa_json_path=$..DeviceHostName,exa_field_name=host"""
    """exa_json_path=$..Status,exa_field_name=status_msg"""
    """exa_json_path=$..EnrollmentTypeMessage,exa_field_name=additional_info"""
    """exa_json_path=$..ScenarioName,exa_field_name=additional_info"""
    """exa_json_path=$..Description,exa_field_name=additional_info"""
    """exa_json_path=$..EventId,exa_field_name=event_code"""
    """exa_json_path=$..FailureReason,exa_field_name=failure_reason"""
    """exa_json_path=$..MessageId,exa_field_name=message_id"""
    """exa_json_path=$..AlertType,exa_field_name=alert_type"""
    """exa_json_path=$..AlertDisplayName,exa_field_name=alert_name"""
    """exa_json_path=$..UPNSuffix,exa_field_name=domain"""
  ]
  DupFields = [ "operation->event_name" 
}
```