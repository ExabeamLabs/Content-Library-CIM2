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
     """"accountName":\s*"(({full_name}[^"\s]+\s[^"]+)|({user}[\w\.\-]{1,40}\$?))"""",
     """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-]{1,40}\$?)(@[^"]+)?))"""",

     """"domainName"+:\s*"+({domain}[^"]+)"""",
     """"logonLocation"+:\s*"+({location}[^"]+)""""
     """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
     """status=({result}[^\s]+)""",
     """msg=.*?\[({alert_source}[^\]]+)\]:"""
  ]
  DupFields = [ "alert_name->alert_subject" ]


}
```