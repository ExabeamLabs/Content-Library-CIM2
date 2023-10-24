#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-graphidentity
  Vendor = "Microsoft" 
  Product = "Microsoft 365"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"riskEventType":"adminConfirmedUserCompromised"""", """"detectedDateTime":"""" ]
  Fields = [
    """"activityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
    """"userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""",
    """"tokenIssuerType":"({token_issuer_type}[^"]+)""",
    """({alert_type}({alert_name}graph-identity-protection-risk-detection))""",
    """"riskLevel":"({alert_severity}[^"]+)""",
    """"activity":"({operation}[^"]+)""",
    """"destinationServiceName":"({app}Office 365)"""",
    """"userId":"({user_sid}[^"]+)""",
    """"riskEventType":"({alert_name}[^"]+)""",
    """"id":"({alert_id}[^"]+)"""",
    """"riskState":"({action}[^"]+)""",
    """"riskDetail":"({additional_info}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```