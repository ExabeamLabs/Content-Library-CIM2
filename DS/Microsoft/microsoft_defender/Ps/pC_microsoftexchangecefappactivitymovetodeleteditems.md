#### Parser Content
```Java
{
Name = "microsoft-exchange-cef-app-activity-movetodeleteditems"
Conditions = [ """CEF:""", """|Exchange Online|""", """|MoveToDeletedItems|""" ]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity-3.Fields}[
    """({user_upn}claims/upn)""",
    """eventName":"({event_name}[^"]+)""""
    """"resultType":"({result}[^"]+)""""
    """exa_regex=({user_upn}claims/upn)""",
    """exa_json_path=$..eventName,exa_field_name=event_name"""
    """exa_json_path=$..resultType,exa_field_name=result"""
  ]
  ParserVersion = "v1.0.0"
}

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
  DupFields = [ "src_host->resource_name" ]
  ParserVersion = v1.0.0
}

{
  Name = microsoft-md-json-alert-trigger-success-threat
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """Azure""", """"SourceSystem":"Microsoft Defender Threat Intelligence"""", """"Action":"alert"""" ]
  Fields = [
     """exa_json_path=$.Action,exa_field_name=action""",
     """exa_json_path=$.Description,exa_field_name=alert_description""",
     """exa_json_path=$.Type,exa_field_name=alert_name""",
     """exa_regex="Description":"(-|({alert_name}[^:,"]+):\s+({alert_description}[^"]+))""""
     """exa_json_path=$.TimeGenerated,exa_field_name=time""",
     """exa_json_path=$.ConfidenceScore,exa_field_name=confidence_level""",
     """exa_json_path=$.ThreatType,exa_field_name=threat_type""",
     """exa_json_path=$.NetworkSourceIP,exa_field_name=src_ip""",
     """exa_json_path=$.FileHashType,exa_field_name=file_hash""",
     """exa_json_path=$.Active,exa_field_name=alert_status""",
     """exa_json_path=$.FileHashValue,exa_field_name=hash_sha256""",
     """exa_json_path=$.Type,exa_field_name=alert_type""",
     """exa_json_path=$.SourceSystem,exa_field_name=alert_source""",
     """exa_json_path=$.AzureTenantId,exa_field_name=tenant_id""",
     """exa_json_path=$.IndicatorId,exa_field_name=indicator"""
  
}
```