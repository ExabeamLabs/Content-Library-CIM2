#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-securitythreatdetected-1
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"src-application-name":"Office 365""""
  """event-name":"security-threat-detected""""
  """"src-event-id""""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s"""
  """"event-name":"({event_name}[^"]+)""""
  """"riskType":"({alert_name}[^"]+)"""
  """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
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