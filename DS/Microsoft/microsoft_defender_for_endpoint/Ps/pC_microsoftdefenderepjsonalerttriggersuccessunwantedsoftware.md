#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-unwantedsoftware
  Product = Microsoft Defender for Endpoint
  Conditions = [ """"category":"UnwantedSoftware"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"Microsoft Defender ATP"""" ]
  ParserVersion = "v1.0.0"

defender-atp-security-alert-events = {
    Vendor = Microsoft
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""",
      """"hostname":"({host}[^"]+)"""",
      """"severity":"({alert_severity}[^"]+)"""",
      """privateIpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """publicIpAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"title":"({alert_name}[^"]+)"""",
      """"category":"({alert_type}[^"]+)"""",
      """"description":"({additional_info}[^\n]+?)\s*","""",
      """userPrincipalName":"({email_address}[^@"]+@[^@"]+)"""",
      """accountName":"({user}[^"]+)""",
      """domainName":"({domain}[^"]+)"""
    
}
```