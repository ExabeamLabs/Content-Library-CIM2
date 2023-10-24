#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-success-reconnotification
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ """"eventType":"ReconNotificationSummaryEvent"""", """"Highlights":["""", """"customerIDString":"""" ]
  Fields = [
  """"eventCreationTime":({time}\d{13}),"""
  """"RuleId":"({alert_id}[^"]+)""""
  """"eventType":"({alert_type}[^"]+)""""
  """"RulePriority":"?({alert_severity}[^"]+)""""
  """"Highlights":\["({additional_info}[^"]+)"\]"""
  ]
  ParserVersion = "v1.0.0"


}
```