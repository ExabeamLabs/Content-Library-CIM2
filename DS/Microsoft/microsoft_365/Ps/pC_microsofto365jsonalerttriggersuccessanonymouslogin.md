#### Parser Content
```Java
{
Name = microsoft-o365-json-alert-trigger-success-anonymouslogin
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"vendor": "Microsoft""""
  """"riskScore":"""
  """"malwareStates":"""
]
Fields = [
  """"userPrincipalName":\s*"({email_address}[^"@]+@[^"]+)"""
  """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"userStates":\s*\[.*?accountName":\s*"({user}[^",]+)"""
  """"accountName":\s*"({user}[^"]+)"""
  """"domainName":\s*"({domain}[^"]+)"""
  """"(eventDateTime|createdDateTime|lastModifiedDateTime)":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"destinationServiceName":\s*"({app}[^"]+)"""
  """"id":\s*"({alert_id}[^"]+)"""
  """"severity":\s*"({alert_severity}[^"]+)"""
  """"description":\s*"({additional_info}[^"]+?)\s*""""
  """"category":\s*"({alert_name}[^"]+)"""
  """"title":\s*"({alert_name}[^"]+?)\s*""""
  """"category":\s*"({alert_type}[^"]+)"""
  """"status":\s*"(unknown|({result}[^"]+))"""
  """"logonLocation":\s*"({location}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```