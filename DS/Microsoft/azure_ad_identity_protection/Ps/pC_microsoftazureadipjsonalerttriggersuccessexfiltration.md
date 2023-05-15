#### Parser Content
```Java
{
Name = microsoft-azureadip-json-alert-trigger-success-exfiltration
  Vendor = Microsoft
  Product = Azure AD Identity Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"category":""", """"Exfiltration"""", """"title":""", """"detectionSource"""", """"serviceSource"""", """"microsoftDataLossPrevention"""", """"Graph Security Alerts"""", """"Azure"""" ]
  Fields = [
    """"id":\s*"({alert_id}[^"]+)"""",
    """"title":\s*"({alert_name}[^"]+)"""",
    """"severity":\s*"({alert_severity}[^"]+)"""",
    """"category":\s*"({alert_type}[^"]+)"""",
    """"description":\s*"({additional_info}[^"]+)"""",
    """"createdDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[^"]+))"""",
    """"userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^\s"@]+)(@[^"]+)?)"""",
    """"domainName":\s*"({domain}[^"]+)"""",
    """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
    """"userAccount":\{[^\}]+?displayName":"({full_name}[^\s"]+\s[^"\(\s]+)\s\([^)"]+\)"""",
    """"userSid":"({user_sid}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```