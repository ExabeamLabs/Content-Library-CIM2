#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-app-activity-success-dlpruleundo"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""Workload":"""
"""PolicyDetails":"""
""""Operation":"DLPRuleUndo""""
]
Fields = [
""""CreationTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)""""
""""Workload":"({app}[^"]+)""""
""""ObjectId":"<?({object}[^"]+?)>?""""
""""Operation":"({operation}[^"]+)""""
""""From":"({email_address}[^@"]+@({email_domain}[^"]+))""""
""""FileOwner":"({full_name}[^\s\/"]+?\s+[^\/"]+?)""""
""""Severity":"({alert_severity}[^"]+)""""
""""IncidentId":"({alert_id}[^"]+)""""
""""RuleName":"({event_name}[^"]+?)""""
""""FileName":"({file_name}[^"]+?)""""
""""PolicyName":"({policy_name}[^"]+)"""
""""Reason":"({additional_info}[^"]+?)""""
]
ParserVersion = "v1.0.0"


}
```