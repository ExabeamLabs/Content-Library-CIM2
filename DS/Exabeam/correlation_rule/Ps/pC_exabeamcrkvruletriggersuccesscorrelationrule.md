#### Parser Content
```Java
{
Name = exabeam-cr-kv-rule-trigger-success-correlationrule
    ParserVersion = "v1.0.0"
    Vendor = Exabeam
    Product = Correlation Rule
    TimeFormat = "epoch_sec"
    trigger_timeFormat = ["epoch_sec", "epoch"]
    Conditions = ["""operation="rule-trigger"""", """alert_source="correlation""""]
    Fields = [
      """usecases="({rule_usecases}[^"]+)"""",
      """mitre_labels="({mitre_labels}[^"]+)"""",
      """rule_description="({rule_description}[^"]+)"""",
      """rule_id="({rule_id}[^"]+)"""",
      """rule="({rule}[^"]+)"""",
      """rule_reason="({rule_reason}[^"]+)"""",
      """rule_type="({rule_type}[^"]+)"""",
      """rule_severity="({rule_severity}[^"]+)"""",
      """dest_host="({dest_host}[^"]+)"""",
      """dest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """src_host="({src_host}[^"]+)"""",
      """src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """url="({url}[^"]+)"""",
      """user="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """trigger_time="({trigger_time}\d{10,13})"""",
      """operation="({operation}[^"]+)"""",
      """alert_source="({alert_source}correlation)"""",
      """tags="({tags}[^"]+)"""",
      """trigger_time="({time}\d{10})"""
      """source_user_entity_id="({source_user_entity_id}[^"]+)""""
      """source_device_entity_id="({source_device_entity_id}[^"]+)""""
      """dest_user_entity_id="({dest_user_entity_id}[^"]+)""""
      """dest_device_entity_id="({dest_device_entity_id}[^"]+)""""
    ]
  

}
```