#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-securitythreatdetected-1
Vendor = "Microsoft"
Product = "Office 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"src-application-name":"Office365""""
  """event-name":"security-threat-detected""""
  """"src-event-id""""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s"""
  """"event-name":"({event_name}[^"]+)""""
  """"riskType":"({alert_name}[^"]+)"""
  """"ipAddress":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
  """"userDisplayName":"({full_name}[^"]+)""""
  """"userPrincipalName":"({email_address}[^@]+@({email_domain}[^"]+))""""
  """"severity":({alert_severity}\d+)"""
  """"requestId":"({alert_id}[^"]+)""""
  """"is-violating":({result}[^,]+)"""
  """"riskEventTypes":\["({alert_name}[^"]+)""""
]
DupFields = [
 "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```