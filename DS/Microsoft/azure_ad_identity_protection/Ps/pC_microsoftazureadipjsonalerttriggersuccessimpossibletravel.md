#### Parser Content
```Java
{
Name = microsoft-azureadip-json-alert-trigger-success-impossibletravel
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure AD Identity Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"category":""", """"ImpossibleTravel"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"IPC"""" ]
  Fields = [
     """"id":\s*"({alert_id}[^"]+)"""",
     """"title":\s*"({alert_name}[^"]+)"""",
     """"severity":\s*"({alert_severity}[^"]+)"""",
     """"category":\s*"({alert_type}[^"]+)"""",
     """"description":\s*"({additional_info}[^"]+)"""",
     """"eventDateTime":\s*"({time}[^"]+)"""",
     """"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[^"]+))"""",
     """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))"""",

     """"domainName"+:\s*"+({domain}[^"]+)"""",
     """"logonLocation"+:\s*"+({location}[^"]+)""""
     """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
  ]


}
```