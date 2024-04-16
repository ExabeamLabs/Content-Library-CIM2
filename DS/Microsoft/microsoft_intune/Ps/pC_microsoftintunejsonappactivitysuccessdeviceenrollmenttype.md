#### Parser Content
```Java
{
Name = microsoft-intune-json-app-activity-success-deviceenrollmenttype
  Vendor = Microsoft
  Product = Microsoft Intune
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"enrolledDateTime":""", """"deviceName":""", """"azureADDeviceId":""", """"azureADRegistered":""", """"deviceEnrollmentType":""" ]
  Fields = [
    """exa_json_path=$.id,exa_field_name=device_id"""
    """exa_json_path=$.deviceEnrollmentType,exa_field_name=operation"""
    """exa_json_path=$.deviceName,exa_field_name=device_name"""
    """exa_json_path=$.lastSyncDateTime,exa_field_name=time"""
    """exa_json_path=$.emailAddress,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """exa_json_path=$.userPrincipalName,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """exa_json_path=$.userDisplayName,exa_field_name=full_name"""
    """exa_json_path=$.userId,exa_field_name=user_sid"""
  ]
  ParserVersion = v1.0.0


}
```