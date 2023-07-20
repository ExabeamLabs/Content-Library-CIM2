#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-dlprulematch-1
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"From":""", """"Workload":""", """"Actions":""", """"DlpRuleMatch"""" ]
  Fields = [
    """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"PolicyName":\s*"(|({alert_type}[^"]+))"(,|\})""",
    """"SensitiveInformation":\s*\[\{[^\}]*?"Location":\s*"(|({additional_info}[^"]+))"(,|\})""",
    """"Severity":\s*"({alert_severity}[^"]+)"""",
    """"IncidentId":\s*"({alert_id}[^"]+)"""",
    """"Actions":\s*\["({result}[^"]+)"""",
    """"RuleName":\s*"(|({alert_name}[^",\(]+?)\s*)("|\()""",
    """"FileName":\s*"(|({file_name}[^"]+))"(,|\})""",
    """"From":\s*"\s*\|?\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)""",
    """"To":\s*\["(({dest_email_address}[^@\]"]+@[^\.\]"]+\.[^\]"]+)|({target}[^\]"]+))"\]""",
    """"To":\s*\[({target}[^\]]+)\]""",
    """src-account-name":"({account_name}[^"]+)""",
    """Operation":\s*"({additional_info}[^"]+)"""",
    """"Workload":\s*"({alert_source}[^",]+)""""
    """\ssuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s"""
  ]
  ParserVersion = "v1.0.0"


}
```