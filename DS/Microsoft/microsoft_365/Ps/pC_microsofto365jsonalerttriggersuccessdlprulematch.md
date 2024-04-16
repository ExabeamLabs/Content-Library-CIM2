#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-dlprulematch
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """DlpRuleMatch"""
  """"From""""
  """"RuleName""""
  """"PolicyName"":""""
]
Fields = [
  """Host Name:\s*({host}[^\s\\]+)"""
  """({event_name}DlpRuleMatch)"""
  """"CreationTime"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"From"+:\s*"+({email_address}[^@]+?@.+?)""""
  """"To"+:\s*\[({recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]]*)\],"""
  """"BCC"+:\s*\[({bcc}[^\]]+)"""
  """"CC"+:\s*\[({cc}[^\]]+)"""
  """"PolicyName"+:\s*"+({alert_type}.*?[^"])""""
  """"Subject"+:\s*"+({alert_subject}.+?)\s*"+,"+To"+:"""
  """"RuleName"+:\s*"+({alert_name}[^",]+)""""
  """"Severity"+:\s*"+({alert_severity}[^"]+)""""
  """"Actions"+:\s*\["+({action}[^"]+)"+\]"""
  """"RecipientCount"+:\s*({recipient_count}\d+)"""
  """"IncidentId"+:\s*"+({alert_id}[^",]+)""""
  """"Workload"+:\s*"+({app}[^",]+)"""
]
ParserVersion = "v1.0.0"


}
```