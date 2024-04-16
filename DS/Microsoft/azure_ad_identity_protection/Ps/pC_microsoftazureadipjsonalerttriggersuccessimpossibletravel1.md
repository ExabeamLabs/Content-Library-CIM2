#### Parser Content
```Java
{
Name = microsoft-azureadip-json-alert-trigger-success-impossibletravel-1
  Product = Azure AD Identity Protection
  Conditions = [ """""category"":""ImpossibleTravel"""", """"title"":""""", """"vendor"":""Microsoft"""", """"provider"":""IPC"""" ]
  ParserVersion = v1.0.0

q-microsoft-security-events = {
    Vendor = Microsoft
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Fields = [
      """"id"+:\s*"+({alert_id}[^"]+)"""",
      """"title"+:\s*"+({alert_name}[^"]+)"""",
      """"severity"+:\s*"+({alert_severity}[^"]+)"""",
      """"category"+:\s*"+({alert_type}[^"]+)"""",
	  """"sourceMaterials"+:\["+({malware_url}[^"]+)"""",
      """"description"+:\s*"+(\\"+)?({additional_info}[^"\]\}]+?)\s*\\?"+[,\]\}]""",
      """"eventDateTime"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"accountName"+:\s*"+\s*(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)|({user}[^\s"]+))"""",
      """aadUserId[^}\]]+?"+accountName"+:\s*"+\s*(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)|({user}[^\s"]+))"""",
      """"logonIp"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"sourceAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"destinationAddress"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"userPrincipalName"+:\s*"+(-|({email_address}([A-Za-z0-9]+[!#$%&'+-/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)|(({user}[^\s"@]+)(@[^"]+)?))"""",
      """"userPrincipalName"+:\s*"+\s*({user_upn}[^"]+?)"""",
      """"domainName"+:\s*"+\s*(-|({domain}[^"]+))"""",
      """"netBiosName"+:\s*"+({src_host}[\w\-\.]+)""",
      """"hostStates"+:[^\}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"hostStates"+:[^\}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
      """"fileStates"+:[^]]+?"+name"+:\s*"+({file_name}[^."]+([\.\w]+)?)"""",
      """"status"+:"+({result}[^"]+)"""",
      """"logonLocation"+:\s*"+({location}[^"]+)""""
    
}
```