#### Parser Content
```Java
{
Name = microsoft-defendercloud-json-alert-trigger-success-assessments
  Vendor = Microsoft
  Product = Microsoft Defender
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
  Conditions= [ """"type":"Microsoft.Security/assessments""", """"action":"""", """"id":""", """"properties":""" ]
  Fields =[
    """exa_json_path=$.properties.timeGenerated,exa_field_name=time""",
    """exa_json_path=$.properties.resourceDetails.resourceName,exa_field_name=src_host""",
    """exa_json_path=$.properties.resourceDetails.resourceName,exa_field_name=resource_name""",
    """exa_json_path=$.properties.resourceDetails.resourceType,exa_field_name=resource_type""",
    """exa_json_path=$.properties.resourceDetails.source,exa_field_name=alert_source""",
    """exa_json_path=$.properties.resourceDetails.id,exa_field_name=resource_path""",
    """exa_json_path=$.properties.displayName,exa_field_name=alert_subject""",
    """exa_json_path=$.properties.description,exa_field_name=additional_info""",
    """exa_json_path=$.properties.impact,exa_field_name=impact""",
    """exa_json_path=$.properties.remediation,exa_field_name=remediation_steps""",
    """exa_json_path=$.properties.category,exa_field_name=category""",
    """exa_json_path=$.properties.status.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.properties.additionalData.query,exa_field_name=query_string""",
    """exa_json_path=$.properties.additionalData.assessedResourceType,exa_field_name=azure_resource_type""",
    """exa_json_path=$.properties.additionalData.scanId,exa_field_name=scan_id""",
    """exa_json_path=$.properties.category,exa_field_name=scan_type""",
    """exa_json_path=$.type,exa_field_name=alert_type""",
    """exa_json_path=$.type,exa_field_name=alert_name""",
    """exa_json_path=$.properties.category,exa_field_name=alert_name""",
    """exa_json_path=$.tenantId,exa_field_name=tenant_id"""
  ]
  ParserVersion = v1.0.0


}
```