#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-graphidentity
  ExtractionType = json
  Vendor = "Microsoft" 
  Product = "Microsoft 365"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """"riskEventType":"adminConfirmedUserCompromised"""", """"detectedDateTime":"""" ]
  Fields = [
    """exa_json_path=$.activityDateTime,exa_field_name=time"""
    """exa_json_path=$.lastUpdatedDateTime,exa_field_name=time"""
    """exa_json_path=$.tokenIssuerType,exa_field_name=token_issuer_type"""
    """exa_regex=({alert_type}({alert_name}graph-identity-protection-risk-detection))"""
    """exa_json_path=$.riskLevel,exa_field_name=alert_severity"""
    """exa_json_path=$.activity,exa_field_name=operation"""
    """exa_json_path=$.destinationServiceName,exa_field_name=app"""
    """exa_json_path=$.userId,exa_field_name=user_sid"""
    """exa_json_path=$.riskEventType,exa_field_name=alert_name"""
    """exa_json_path=$.id,exa_field_name=alert_id"""
    """exa_json_path=$.riskState,exa_field_name=action"""
    """exa_json_path=$.riskDetail,exa_field_name=additional_info"""
    """exa_json_path=$.userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```