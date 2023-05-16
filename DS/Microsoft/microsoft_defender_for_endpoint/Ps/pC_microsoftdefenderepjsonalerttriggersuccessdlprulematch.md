#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-dlprulematch
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"From":""", """"Workload":""", """"Actions":""", """"DLPRuleMatch"""" ]
  Fields = [
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"PolicyName":\s*"(|({alert_type}[^"]+))"(,|\})""",
    """"SensitiveInformation":\s*\[\{[^\}]*?"Location":\s*"(|({additional_info}[^"]+))"(,|\})""",
    """"Severity":\s*"({alert_severity}[^"]+)"""",
    """"IncidentId":\s*"({alert_id}[^"]+)"""",
    """"Actions":\s*\["({result}[^"]+)"""",
    """"RuleName":\s*"(|({alert_name}[^",\(]+?)\s*)("|\()""",
    """"FileName":\s*"(|({file_name}[^"]+))"(,|\})""",
    """"From":\s*"(({email_address}[^@"]+?@[^\."]+\.[^"]+)|({user}[^@"]+)@({domain}[^@"]+))""", 
    """"To":\s*\["?({target}[^\]"]+?)"?\]""",
    """"Workload":\s*"({alert_source}[^",]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```