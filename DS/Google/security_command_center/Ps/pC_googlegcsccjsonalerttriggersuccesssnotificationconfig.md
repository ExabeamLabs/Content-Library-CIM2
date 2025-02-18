#### Parser Content
```Java
{
Name = google-gcscc-json-alert-trigger-successs-notificationconfig
  ParserVersion = v1.0.0
  Vendor = Google
  Product = Security Command Center
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """"notificationConfigName":""", """"finding":""", """"category":""", """"findingClass":""", """"severity":""", """"orgID":""" ]
  Fields = [
    """exa_json_path=$.finding.eventTime,exa_field_name=time""",
    """exa_json_path=$.finding.state,exa_field_name=incident_status"""
    """exa_json_path=$.finding.category,exa_field_name=alert_name"""
    """exa_json_path=$.finding.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.finding.findingClass,exa_field_name=alert_type"""
    """exa_json_path=$.finding.sourceProperties.detectionCategory.technique,exa_field_name=technique"""
    """exa_json_path=$.finding.sourceProperties.properties.vpcViolation.userEmail,exa_field_name=email_address"""
    """exa_json_path=$.finding.sourceProperties.Recommendation,exa_field_name=remediation_steps"""
    """exa_json_path=$.finding.nextSteps,exa_field_name=remediation_steps"""
    """exa_json_path=$.finding.description,exa_field_name=alert_reason"""
    """exa_json_path=$.finding.sourceProperties.Explanation,exa_field_name=alert_reason"""
    """exa_json_path=$.resource.name,exa_field_name=resource_name"""
    """exa_json_path=$.resource.cloudProvider,exa_field_name=provider_name"""
    """exa_json_path=$.resource.service,exa_field_name=service_name"""
    """exa_json_path=$..callerIp,exa_field_name=src_ip"""
  ]


}
```