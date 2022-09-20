#### Parser Content
```Java
{
Name = exabeam-cr-kv-alert-trigger-success-correlationrule
ParserVersion = "v1.0.0"
Vendor = Exabeam
Product = Correlation Rule
TimeFormat = "epoch"
Conditions = [ """operation="alert-trigger"""" , """alert_source="correlation"""" ]
Fields = [
"""usecases="({rule_usecases}[^"]+)"""",
"""mitre_labels="({mitre_labels}[^"]+)"""",
"""alert_severity="({alert_severity}[^"]+)"""",
"""rule_severity="({rule_severity}[^"]+)"""",
"""alert_source="({alert_source}correlation)"""",
"""alert_name="({alert_name}[^"]+)"""",
"""alert_type="({alert_type}[^"]+)"""",
"""dest_host="({dest_host}[^"]+)"""",
"""dest_ip="({dest_ip}[^"]+)"""",
"""operation="({operation}[^"]+)"""",
"""rule_description="({rule_description}[^"]+)"""",
"""rule_id="({rule_id}[^"]+)"""",
"""rule="({rule}[^"]+)"""",
"""rule_reason="({rule_reason}[^"]+)"""",
# """rule_type="({rule_type}[^"]+)"""",
"""src_host="({src_host}[^"]+)"""",
"""src_ip="({src_ip}[^"]+)"""",
"""trigger_time="({trigger_time}\d+)"""",
"""url="({url}[^"]+)"""",
"""user="({user}[^"]+)""""	  
]


}
```