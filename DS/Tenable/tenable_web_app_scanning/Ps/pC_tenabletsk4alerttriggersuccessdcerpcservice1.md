#### Parser Content
```Java
{
Name = tenable-t-sk4-alert-trigger-success-dcerpcservice-1
  Vendor = Tenable
  Product = Tenable Web App Scanning
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """"scan":""", """"indexed":""", """"synopsis":""", """"hostname":""", """"publication_date":""", """"exploit_available":""" ]
  Fields = [
    """started_at"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"indexed"+:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"hostname"+:\s*"+({host}[^"]+)""",
    """"+ipv4"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+severity"+:\s*"+({alert_severity}[^"]+)""",
    """"name"+:\s*"+({alert_name}[^"]+)""",
    """"synopsis"+:\s*"+({alert_subject}[^"]+)""",
    """"+description"+:\s*"+({additional_info}[^"]+?)"+""",
    """cvss_base_score"+:\s*({cvss_base_score}[^,]+)""",
    """cvss3_impact_score"+:\s*({original_risk_score}\d+)""",
    """exploit_code_maturity"+:\s*"+({exploit_code_maturity}[^"]+)""",
    """see_also"+:\s*\["*(|({see_also}[^\]]+?))"*\]""",
    """cve"+:\s*\[({cve_id}[^\]]+)\]""",
    """protocol"+:\s*"+({protocol}[^"]+)""",
    """"state"+:\s*"+({alert_status}[^"]+)""",
    """"solution"+:\s*"+((?i)n\/a|({solution}[^"]+))"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.scan.started_at,exa_field_name=time"""
    """exa_json_path=$.scan.indexed,exa_field_name=time"""
    """exa_json_path=$.asset.hostname,exa_field_name=host"""
    """exa_json_path=$.plugin.name,exa_field_name=alert_name"""
    """exa_json_path=$.plugin.synopsis,exa_field_name=alert_subject"""
    """exa_json_path=$.asset.ipv4,exa_field_name=src_ip"""
    """exa_json_path=$.port.protocol,exa_field_name=protocol"""
    """exa_json_path=$.state,exa_field_name=alert_status"""
    """exa_json_path=$.plugin.solution,exa_field_name=solution"""
    """exa_json_path=$.plugin.description,exa_field_name=additional_info"""
    """exa_json_path=$.plugin.cvss_base_score,exa_field_name=cvss_base_score""",
    """exa_json_path=$.plugin.vpr.drivers.cvss3_impact_score,exa_field_name=original_risk_score""",
    """exa_json_path=$.plugin.vpr.drivers.exploit_code_maturity,exa_field_name=exploit_code_maturity""",
    """exa_json_path=$.plugin.see_also,exa_field_name=see_also""",
    """exa_json_path=$.plugin.cve,exa_field_name=cve_id"""
  ]
  DupFields = ["alert_name->alert_type"]
  ParserVersion = "v1.0.0"


}
```