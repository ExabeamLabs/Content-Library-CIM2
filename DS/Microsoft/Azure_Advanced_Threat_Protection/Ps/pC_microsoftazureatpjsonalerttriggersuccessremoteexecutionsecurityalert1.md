#### Parser Content
```Java
{
Name = microsoft-azureatp-json-alert-trigger-success-remoteexecutionsecurityalert-1
  Product = Azure Advanced Threat Protection
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"RemoteExecutionSecurityAlert"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"Azure Advanced Threat Protection"""" ]

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