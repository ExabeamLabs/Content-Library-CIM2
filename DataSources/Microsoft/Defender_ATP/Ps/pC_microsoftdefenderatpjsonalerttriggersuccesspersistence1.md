#### Parser Content
```Java
{
Name = microsoft-defenderatp-json-alert-trigger-success-persistence-1
  Product = Defender ATP
  Conditions = [ """"category":"Persistence"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"Microsoft Defender ATP"""" ]
  ParserVersion = "v1.0.0"

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