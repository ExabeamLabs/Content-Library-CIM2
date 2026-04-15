#### Parser Content
```Java
{
Name = "microsoft-exchange-kv-app-activity-softdelete"
Conditions = [
"""WORKLOAD=Exchange"""
"""COMMAND=SoftDelete"""
"""CLIENTPROCESSNAME="""
"""TS="""
]
ParserVersion = "v1.0.0"

cef-microsoft-app-activity-3.Fields}[
    """({user_upn}claims/upn)""",
    """eventName":"({event_name}[^"]+)""""
    """"resultType":"({result}[^"]+)""""
    """exa_regex=({user_upn}claims/upn)""",
    """exa_json_path=$..eventName,exa_field_name=event_name"""
    """exa_json_path=$..resultType,exa_field_name=result"""
    """exa_json_path=$.identity.claim.appid,exa_field_name=app_id"""
    """exa_json_path=$..authorization.evidence.scope,exa_field_name=authorization_scope"""
    """exa_json_path=$..identity,exa_regex="roleDefinitionId\\?"+:\s*\\?"+({role_definition_id}[^"]+)\\?""""
    """exa_json_path=$..identity,exa_regex="principalId\\?"+:\s*\\?"+({principal_id}[^"]+)\\?""""
    """exa_json_path=$..identity,exa_regex="principalType\\?"+:\s*\\?"+({principal_type}[^"]+)\\?""""
    """exa_json_path=$..identity.claims.appid,exa_field_name=app_id""",
    """exa_json_path=$..identity.claims.ver,exa_field_name=app_version""",
    """exa_json_path=$..RoleLocation,exa_field_name=region""",
    """exa_json_path=$..resultType,exa_field_name=result""",
    """exa_json_path=$.properties.serviceRequestId,exa_field_name=service_id"""
    """exa_json_path=$.properties.eventCategory,exa_field_name=event_category"""
    """exa_json_path=$.properties.entity,exa_regex=({resource}({resource_path}[^"]+)\/({resource_name}[^"]+)|[^"]+)"""

  ]
  ParserVersion = "v1.0.0"
}

{
  Name = microsoft-defendercloud-json-alert-trigger-success-assessments
  Vendor = Microsoft
  Product = Microsoft Defender for Cloud
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
{
    Name = microsoft-sentinel-json-security-alert-trigger-securityalert
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Microsoft Sentinel
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    start_timeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    end_timeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    Conditions = [ """"Type":"SecurityAlert"""", """"VendorName":"Microsoft"""", """"AlertSeverity":""", """"AlertType":""", """"AlertName":""", """"Description":"""]
    Fields=[
     """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_json_path=$.Description,exa_field_name=description""",
    """exa_json_path=$.CompromisedEntity,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_host}[\w\-\.]+))""",
    """exa_json_path=$.ProductName,exa_field_name=product_name""",
    """exa_json_path=$.AlertSeverity,exa_field_name=alert_severity""",
    """exa_json_path=$.AlertType,exa_field_name=alert_type""",
    """exa_json_path=$.SystemAlertId,exa_field_name=alert_id""",
    """exa_json_path=$.Status,exa_field_name=alert_status""",
    """exa_json_path=$.Tactics,exa_field_name=tactic""",
    """exa_json_path=$.AlertName,exa_field_name=alert_name""",
    """exa_json_path=$.Techniques,exa_regex=\["({technique}[^\]]+)\"]""",
    """exa_json_path=$.StartTime,exa_field_name=start_time""",
    """exa_json_path=$.EndTime,exa_field_name=end_time""",
    """exa_json_path=$.ProviderName,exa_field_name=provider_name""",
    """exa_json_path=$.Type,exa_field_name=table_name""",
    """exa_json_path=$.AlertLink,exa_field_name=link""",
    """exa_json_path=$.ConfidenceScore,exa_field_name=original_risk_score""",
    """exa_json_path=$.ExtendedProperties,exa_field_name=more_info""",
    """exa_json_path=$.Entities,exa_field_name=additional_info"""
    
}
```