#### Parser Content
```Java
{
Name = "symantec-endpointprotection-kv-alert-trigger-success-rule"
Conditions = [
"""vendor_product="Symantec Endpoint Protection""""
"""signature="Rule:"""
]
DupFields = [
"alert_name->alert_type"
"process_guid->process_id"
]
ParserVersion = "v1.0.0"


}
```