#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-securitythreatdetected-1
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
  """"src-application-name":"Office 365""""
  """event-name":"security-threat-detected""""
  """"src-event-id""""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s"""
  """"lastUpdatedDateTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+(\.\d{1,7})?Z)"""
  """"event-name":"({event_name}[^"]+)""""
  """"riskType":"({alert_type}({alert_name}[^"]+))"""
  """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"userDisplayName":"({full_name}[^"]+)""""
  """"userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
  """"severity":({alert_severity}\d+)"""
  """"requestId":"({alert_id}[^"]+)""""
  """"is-violating":({result}[^,]+)"""
  """"riskEventTypes":\["({alert_type}({alert_name}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```