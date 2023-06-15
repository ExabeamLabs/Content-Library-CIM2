#### Parser Content
```Java
{
Name = microsoft-m365auditlogs-json-alert-trigger-threatmanagement
  ParserVersion = v1.0.0
  Product = M365 Audit Logs
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category": "ThreatManagement"""", """"title": """, """"vendor": "Microsoft"""", """"provider": "Office 365 Security and Compliance""""  ]

json-microsoft-security-events = {
     Vendor = Microsoft
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
     Fields = [
       """"id":\s*"({alert_id}[^"]+)""""
       """"title":\s*"({alert_name}[^"]+)""""
       """"severity":\s*"({alert_severity}[^"]+)""""
       """"category":\s*"({alert_type}[^"]+)""""
       """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
       """"sourceMaterials":\["({additional_info}[^"]+)"""",
       """"eventDateTime":\s*"({time}[^"]+)""""
       """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
       """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
       """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
       """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))""""
       """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
       """"domainName"+:\s*"+(-|({domain}[^"]+))""""
       """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
       """"fqdn"+:\s*"+({src_host}[^"]+)""""
       """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
       """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
       """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
       """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
       """"destinationServiceName":"({app}[^"]+)""""
       """"status":"({result}[^"]+)"""",
       """"logonLocation"+:\s*"+({location}[^"]+)""""
     
}
```