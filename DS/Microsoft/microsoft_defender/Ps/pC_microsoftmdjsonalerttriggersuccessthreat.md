#### Parser Content
```Java
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
  ]


}
```