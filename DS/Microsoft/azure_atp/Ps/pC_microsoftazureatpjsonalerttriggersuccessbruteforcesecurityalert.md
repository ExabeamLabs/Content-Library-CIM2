#### Parser Content
```Java
{
Name = "microsoft-azureatp-json-alert-trigger-success-bruteforcesecurityalert"
ParserVersion = "v1.0.0"
Product = "Azure ATP"
Conditions = [""""category":"BruteForceSecurityAlert"""",""""title":""",""""vendor":""",""""Microsoft""""]

json-microsoft-security-events}{
Name = "microsoft-azureatp-json-alert-trigger-success-bruteforcesecurityalert"
ParserVersion = "v1.0.0"
Product = "Azure ATP"
Conditions = [""""category":"BruteForceSecurityAlert"""",""""title":""",""""vendor":""",""""Microsoft""""json-microsoft-security-events = {
     Vendor = Microsoft
     ExtractionType = json
     TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSZ", "yyyy-MM-dd'T'HH:mm:ss.SZ"]
     Fields = [
      """"id":\s*"({alert_id}[^"]+)""""
       """"title":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?""""
       """"severity":\s*"({alert_severity}[^"]+)""""
       """"category":\s*"({alert_type}[^"]+)""""
       """"description":\s*"({additional_info}[^}
}
```