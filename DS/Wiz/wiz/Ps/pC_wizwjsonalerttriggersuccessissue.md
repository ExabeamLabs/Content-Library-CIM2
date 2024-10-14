#### Parser Content
```Java
{
Name = wiz-w-json-alert-trigger-success-issue
  Vendor = Wiz
  Product = Wiz
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ" ]
  Conditions = [ """"source":"ISSUE"""", """"updatedFields":"""", """"status":"""", """"subscriptionName":"""", """"changedBy":"Wiz"""" ]
  Fields = [
         """exa_json_path=$.issue.created,exa_field_name=time"""
         """exa_json_path=$.issue.severity,exa_field_name=alert_severity"""
         """exa_json_path=$.control.name,exa_field_name=alert_name""",
         """exa_json_path=$.control.description,exa_field_name=additional_info""",
         """exa_json_path=$.trigger.updatedFields,exa_field_name=additional_info""",     
         """exa_json_path=$.trigger.ruleName,exa_field_name=rule""",
         """exa_json_path=$.trigger.ruleId,exa_field_name=rule_id""",
         """exa_json_path=$.resource.subscriptionId,exa_field_name=subscription_id"""
         """exa_json_path=$.resource.name,exa_regex=\s*"({host}[\w\-\.]+)"""
         """exa_json_path=$.resource.type,exa_field_name=host_type"""
         """exa_json_path=$.resource.subscriptionName,exa_field_name=resource_name"""
         """exa_json_path=$.resource.subscriptionId,exa_field_name=aws_account"""
  ]
  DupFields = [ "rule->alert_type" ]
  ParserVersion = v1.0.0


}
```