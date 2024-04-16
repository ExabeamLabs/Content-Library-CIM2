#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-alert-trigger-success-sensitivefileread"
  ExtractionType = json
  Conditions = [ """DeviceEvents"""", """"ActionType":"SensitiveFileRead"""" ]
  DupFields = ["action->alert_name", "category->alert_type"]
  ParserVersion = "v1.0.0"


}
```