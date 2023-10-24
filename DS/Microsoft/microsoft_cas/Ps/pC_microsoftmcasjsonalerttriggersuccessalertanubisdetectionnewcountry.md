#### Parser Content
```Java
{
Name = "microsoft-mcas-json-alert-trigger-success-alertanubisdetectionnewcountry"
ParserVersion = "v1.0.0"
Product = "Microsoft CAS"
Conditions = [
  """"category":"""
  """"MCAS_ALERT_ANUBIS_DETECTION_NEW_COUNTRY""""
  """"title":"""
  """"vendor":"""
  """"Microsoft""""
  """"provider":"""
  """"MCAS""""
]

json-microsoft-security-events = {
     Vendor = Microsoft
     TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
     Fields = [
       """"id":\s*"({alert_id}[^"]+)""""
       """"title":\s*"({alert_name}[^"]+)""""
       """"severity":\s*"({alert_severity}[^"]+)""""
       """"category":\s*"({alert_type}[^"]+)""""
       """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
       """"sourceMaterials":\["({additional_info}[^"]+)"""",
       """"eventDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)""""
       """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"<]+)|({email_address}[^"@]+@[^"]+)|([^\."]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?))("|\s+<)"""
       """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"<]+)|({email_address}[^"@]+@[^"]+)|([^\."]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?))("|\s+<)"""
       """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
       """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-]{1,40}\$?)(@[^"]+)?))""""
       """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
       """"domainName"+:\s*"+(-|({domain}[^"]+))""""
       """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
       """"fqdn"+:\s*"+({src_host}[\w\-\.]+)"""
       """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
       """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
       """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
       """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
       """"destinationServiceName":"({app}[^"]+)""""
       """"status":"({result}[^"]+)"""",
       """"logonLocation"+:\s*"+({location}[^"]+)""""
     
}
```