#### Parser Content
```Java
{
Name = exabeam-cr-kv-rule-trigger-success-correlationrule
ParserVersion = "v1.0.0"
Vendor = Exabeam
Product = Correlation Rule
TimeFormat = "epoch"
Conditions = [ """operation="rule-trigger"""", """alert_source="correlation"""" ]
Fields = [
"""usecases="({rule_usecases}[^"]+)"""",
"""mitre_labels="({mitre_labels}[^"]+)"""",
"""rule_description="({rule_description}[^"]+)"""",
"""rule_id="({rule_id}[^"]+)"""",
"""rule="({rule}[^"]+)"""",
"""rule_reason="({rule_reason}[^"]+)"""",
# """rule_type="({rule_type}[^"]+)"""",
"""rule_severity="({rule_severity}[^"]+)"""",
"""dest_host="({dest_host}[^"]+)"""",
"""dest_ip="({dest_ip}[^"]+)"""",
"""src_host="({src_host}[^"]+)"""",
"""src_ip="({src_ip}[^"]+)"""",
"""url="({url}[^"]+)"""",
"""user="({user}[^"]+)"""",
"""trigger_time="({trigger_time}\d+)"""",
"""operation="({operation}[^"]+)"""",
"""alert_source="({alert_source}correlation)""""  	  
]


}
```