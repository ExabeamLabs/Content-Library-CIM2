#### Parser Content
```Java
{
Name = microsoft-defenderatp-json-alert-trigger-success-suspiciousactivity
  Product = Defender ATP
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"SuspiciousActivity"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"Microsoft 365 Defender"""" ]

defender-atp-security-alert-events = {
    Vendor = Microsoft
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
      """"hostname":"({host}[^"]+)"""",
      """"severity":"({alert_severity}[^"]+)"""",
      """privateIpAddress":"({src_ip}[a-fA-F\d:.]+)"""",
      """publicIpAddress":"({dest_ip}[a-fA-F\d:.]+)"""",
      """"title":"({alert_name}[^"]+)"""",
      """"category":"({alert_type}[^"]+)"""",
      """"description":"({additional_info}[^\n]+?)\s*","""",
      """userPrincipalName":"({email_address}[^@"]+@[^@"]+)"""",
      """accountName":"({user}[^"]+)""",
      """domainName":"({domain}[^"]+)"""
    
}
```