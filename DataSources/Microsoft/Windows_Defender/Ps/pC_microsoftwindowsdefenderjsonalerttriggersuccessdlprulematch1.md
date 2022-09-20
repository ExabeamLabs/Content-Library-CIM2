#### Parser Content
```Java
{
Name = microsoft-windowsdefender-json-alert-trigger-success-dlprulematch-1
  Vendor = Microsoft
  Product = Windows Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"From":""", """"Workload":""", """"Actions":""", """"DlpRuleMatch"""" ]
  Fields = [
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"PolicyName":\s*"(|({alert_type}[^"]+))"(,|\})""",
    """"SensitiveInformation":\s*\[\{[^\}]*?"Location":\s*"(|({additional_info}[^"]+))"(,|\})""",
    """"Severity":\s*"({alert_severity}[^"]+)"""",
    """"IncidentId":\s*"({alert_id}[^"]+)"""",
    """"Actions":\s*\["({action}[^"]+)"""",
    """"RuleName":\s*"(|({alert_name}[^",\(]+?)\s*)("|\()""",
    """"FileName":\s*"(|({file_name}[^"]+))"(,|\})""",
    """"From":\s*"({email_address}[^@"]+?@[^@"]+?)"""",
    """"To":\s*\["(({dest_email_address}[^@\]"]+@[^\.\]"]+\.[^\]"]+)|({target}[^\]"]+))"\]""",
    """src-account-name":"({account_name}[^"]+)""",
    """Operation":\s*"({additional_info}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```