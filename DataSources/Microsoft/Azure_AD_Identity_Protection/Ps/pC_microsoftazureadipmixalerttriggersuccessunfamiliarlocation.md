#### Parser Content
```Java
{
Name = microsoft-azureadip-mix-alert-trigger-success-unfamiliarlocation
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure AD Identity Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"category":""", """"UnfamiliarLocation"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"IPC""""  ]
  Fields = [
     """"id":\s*"({alert_id}[^"]+)"""",
     """"title":\s*"({alert_name}[^"]+)"""",
     """"severity":\s*"({alert_severity}[^"]+)"""",
     """"category":\s*"({alert_type}[^"]+)"""",
     """"description":\s*"({additional_info}[^"]+)"""",
     """"eventDateTime":\s*"({time}[^"]+)"""",
     """"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[^"]+))"""",
     """"logonIp":\s*"({src_ip}[a-fA-F:\d.]+)"""",
     """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))"""",

     """"domainName"+:\s*"+({domain}[^"]+)"""",
     """"logonLocation"+:\s*"+({location}[^"]+)""""
     """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
  ]


}
```