#### Parser Content
```Java
{
Name = microsoft-o365-cef-alert-trigger-success-alertdetected
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
""""Operation":"DlpRuleMatch""""
"""destinationServiceName =Office 365"""
]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d\.\d\d\d)""""
""""FromPerson":"({email_address}[^\@]+\@[^"]+)""""
""""Id":"({user_id}[^"]+)""""
"""({alert_type}DlpRuleMatch)"""
""""PolicyName":"({alert_name}[^"]+)""""
""""ToPerson":"({recipient}[^\@]+\@[^"]+)""""
""""RuleName":"({additional_info}[^"]+)""""
""""Location":"(Message Body|({file_name}[^"]+))""""
""""IncidentId":"({alert_id}[^"]+)""""
""""Severity":"({alert_severity}[^"]+)""""
]
DupFields = [
"recipient->target"
"alert_name->event_name"
]
ParserVersion = "v1.0.0"


}
```