#### Parser Content
```Java
{
Name = tenable-t-sk4-alert-trigger-success-dcerpcservice-1
  Vendor = Tenable
  Product = Tenable Web App Scanning
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"scan":""", """"completed_at":""", """"synopsis":""", """fqdn":""", """"publication_date":""" ]
  Fields = [
    """started_at"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"hostname"+:\s*"+({host}[^"]+)""",
    """"+ipv4"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"+severity"+:\s*"+({alert_severity}[^"]+)""",
    """"name"+:\s*"+({alert_name}[^"]+)""",
    """"+description"+:\s*"+({additional_info}[^"]+?)"+""",
    """cvss_base_score"+:\s*({cvss_base_score}[^,]+)""",
    """cvss3_impact_score"+:\s*({original_risk_score}\d+)""",
    """exploit_code_maturity"+:\s*"+({exploit_code_maturity}[^"]+)""",
    """see_also"+:\s*\["*(|({see_also}[^\]]+?))"*\]""",
    """cve"+:\s*\[({cve_id}[^\]]+)\]""",
    """protocol"+:\s*"+({protocol}[^"]+)""",
    """"state"+:\s*"+({action}[^"]+)""",
    """"solution"+:\s*"+((?i)n\/a|({solution}[^"]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```