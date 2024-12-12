#### Parser Content
```Java
{
Name = "microsoft-365defender-json-endpoint-activity-success-publish-identityinfo"
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ExtractionType = "json"
  Conditions = [ """"category":"AdvancedHunting-IdentityInfo"""", """"operationName":"Publish"""", """"AccountUpn":""" ]
  Fields = [
    """exa_json_path=$.operationName,exa_field_name=operation"""
    """exa_json_path=$.time,exa_field_name=time"""
    """exa_json_path=$.category,exa_field_name=category"""
    """exa_json_path=$.properties.AccountUpn,exa_field_name=user_upn"""
    """exa_json_path=$.properties.CloudSid,exa_field_name=user_sid"""
    """exa_json_path=$.properties.Department,exa_field_name=department"""
    """exa_json_path=$.properties.JobTitle,exa_field_name=employee_title"""
    """exa_json_path=$.properties.City,exa_field_name=city"""
    """exa_json_path=$.properties.EmailAddress,exa_field_name=email_address"""
    """exa_json_path=$.properties.Country,exa_field_name=country"""
    """exa_json_path=$.properties.AccountName,exa_field_name=full_name"""
  ]
  ParserVersion = "v1.0.0"


}
```