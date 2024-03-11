#### Parser Content
```Java
{
Name = f5-silverline-kv-alert-trigger-ipi
  ParserVersion = v1.0.0
  Product = F5 Silverline
  Vendor = F5
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ type=ipi, """, """ ip_intelligence_policy_name=""", """ ip_intelligence_threat_name=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s+({host}\S+)\s+""",
    """ip_intelligence_policy_name="({policy_name}[^"]+)"""",
    """ip_intelligence_threat_name="(\[\")?({rule}[^"]+?)\\?"""",
    """ip_protocol="({protocol}[^"]+)"""",
    """severity="({alert_severity}[^"]+)"""",
    """source_ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """source_port="({src_port}\d+)"""",
    """action="({operation}[^"]+)"""",
    """attack_type="({rule_type}[^"]+)"""",
  ]
  # DupFields = ["rule_type->alert_type" , "policy_name->alert_name"]
  DupFields = ["policy_name->alert_name"]


}
```