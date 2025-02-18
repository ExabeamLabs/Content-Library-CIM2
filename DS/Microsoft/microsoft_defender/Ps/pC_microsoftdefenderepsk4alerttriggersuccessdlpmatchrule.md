#### Parser Content
```Java
{
Name = "microsoft-defenderep-sk4-alert-trigger-success-dlpmatchrule"
Vendor = "Microsoft"
Product = "Microsoft Defender"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
""""Operation":"DLPRuleMatch""""
""""RuleName":""""
""""PolicyName":""""
""""IncidentId":""""
]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d\.\d\d\d)""""
""""PolicyName":\s*"(|({alert_type}[^"]+))"(,|\})"""
""""SensitiveInformation":\s*\[\{[^\}]*?"Location":\s*"(|({additional_info}[^"]+))"(,|\})"""
""""SensitiveInformationTypeName":"({additional_info}[^"]+)""""
""""Severity":\s*"({alert_severity}[^"]+)""""
""""IncidentId":\s*"({alert_id}[^"]+)""""
""""RuleName":\s*"(|({alert_name}[^",\(]+?)\s*)("|\()"""
""""FileName":\s*"(|({file_name}[^"]+))"(,|\})"""
""""FileFrom":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
""""FileOwner":"({full_name}[^\s\/"]+?\s+[^\/"]+?)\/({domain}[^"]+?)""""
]
ParserVersion = "v1.0.0"


}
```