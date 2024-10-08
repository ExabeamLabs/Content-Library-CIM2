#### Parser Content
```Java
{
Name = tenable-t-json-alert-trigger-success-dcerpcservice
  ExtractionType = json
  Vendor = Tenable
  Product = Tenable Web App Scanning
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"scan":""", """"completed_at":""", """"synopsis":""",""""IO_address":""", """"asset_fqdn":""", """"publication_date":""" ]
  Fields = [
    """exa_json_path=$.scan.started_at,exa_field_name=time"""
    """exa_json_path=$.asset_fqdn,exa_field_name=host"""
    """exa_json_path=$.ipv4,exa_field_name=src_ip"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.plugin.name,exa_field_name=alert_name"""
    """exa_json_path=$.plugin.description,exa_field_name=additional_info"""
    """exa_json_path=$.plugin.vpr..cvss3_impact_score,exa_field_name=original_risk_score"""
    """exa_json_path=$.plugin.vpr..exploit_code_maturity,exa_field_name=exploit_code_maturity"""
    """exa_json_path=$.plugin.see_also,exa_field_name=see_also"""
    """exa_json_path=$.plugin.cve,exa_field_name=cve_id"""
    """exa_json_path=$.port.protocol,exa_field_name=protocol"""
    """exa_json_path=$.state,exa_field_name=action"""
    """exa_json_path=$.plugin.solution,exa_field_name=solution"""
  ]
  ParserVersion = "v1.0.0"


}
```