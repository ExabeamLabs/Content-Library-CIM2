#### Parser Content
```Java
{
Name = pan-prisma-json-alert-trigger-success-prismacloud
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [""""alertRuleName":""", """"app":"Prisma Cloud Alert Notification"""", """"source":"Prisma Cloud"""", """"policyName":"""]
  Fields = [ 
    """exa_json_path=$.message.policyName,exa_field_name=alert_name"""
    """exa_json_path=$.message.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.message.alertId,exa_field_name=alert_id"""
    """exa_json_path=$.message.callbackUrl,exa_field_name=additional_info"""
    """exa_json_path=$.message.source,exa_field_name=app"""
    """exa_json_path=$.message.resource.url,exa_field_name=url"""
    """exa_json_path=$.message.policyId,exa_field_name=policy_id"""
    """exa_json_path=$.message.accountName,exa_field_name=user"""
    """exa_json_path=$.message.alertRuleName,exa_field_name=alert_type"""
    """exa_regex=(({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ))"""
    """exa_regex=((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```