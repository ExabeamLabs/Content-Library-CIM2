#### Parser Content
```Java
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
    ]


}
```