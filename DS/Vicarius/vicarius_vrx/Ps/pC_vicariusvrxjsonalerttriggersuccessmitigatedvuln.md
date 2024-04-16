#### Parser Content
```Java
{
Name = vicarius-vrx-json-alert-trigger-success-mitigatedvuln
  ParserVersion = v1.0.0
  Conditions = [ """"analyticsEventPairAnalyticsEventAction":"IncidentEvent"""", """"analyticsEventCreatedAt"""", """"incidentEventIncidentEventType":"MitigatedVulnerability"""" ]
  
vicarius-vrx-json-events-template = {
  Vendor = Vicarius
  Product = Vicarius vRx
  ExtractionType = json
  TimeFormat = "epoch"
  Fields = [
     """exa_json_path=$.analyticsEventCreatedAt,exa_field_name=time""",
     """exa_json_path=$.analyticsEventAuthenticatedModelAbs.endpointName,exa_field_name=src_host""",
     """exa_json_path=$.incidentEventIncidentEventType,exa_field_name=alert_type""",
     """exa_json_path=$.incidentEventOrganizationPublisherProducts.organizationPublisherProductsProduct.productName,exa_field_name=additional_info""",
     """exa_json_path=$.incidentEventVulnerability.vulnerabilitySummary,exa_field_name=alert_name""",
     """exa_json_path=$.incidentEventVulnerability.vulnerabilitySensitivityLevel.sensitivityLevelName,exa_field_name=alert_severity""",
     """exa_json_path=$.incidentEventOrganizationPublisherOperatingSystems.organizationPublisherOperatingSystemsOperatingSystem.operatingSystemName,exa_field_name=os"""
     """exa_json_path=$.vulnerabilityId,exa_field_name=event_code""",
     """exa_json_path=$.analyticsEventAuthenticatedModelAbs.endpointOrganization.userId,exa_field_name=user_id""",
     """exa_json_path=$.analyticsEventAuthenticatedModelAbs.endpointOrganization.organizationDomainPrefix,exa_field_name=src_domain""",
     """exa_json_path=$.incidentEventOrganizationPublisherProducts.organizationPublisherProductsOrganization.userId,exa_field_name=user_id""",
     """exa_json_path=$.incidentEventOrganizationPublisherProducts.organizationPublisherProductsOrganization.organizationDomainPrefix,exa_field_name=src_domain""",
     """exa_json_path=$.incidentEventVulnerability.vulnerabilityExternalReference.externalReferenceExternalId,exa_field_name=additional_info"""
  ]
 
}
```