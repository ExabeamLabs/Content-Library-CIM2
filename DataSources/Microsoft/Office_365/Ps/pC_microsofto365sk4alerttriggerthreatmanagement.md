#### Parser Content
```Java
{
Name = microsoft-o365-sk4-alert-trigger-threatmanagement
  Vendor = Microsoft
  Product = Office 365
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"category":"ThreatManagement"""", """"title":""", """"vendor":"Microsoft"""", """"provider":"Office 365 Security and Compliance""""  ]
  ParserVersion = "v1.0.0"

json-microsoft-security-events = {
     Vendor = Microsoft
     TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
     Fields = [
       """"id":\s*"({alert_id}[^"]+)""""
       """"title":\s*"({alert_name}[^"]+)""""
       """"severity":\s*"({alert_severity}[^"]+)""""
       """"category":\s*"({alert_type}[^"]+)""""
       """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
       """"eventDateTime":\s*"({time}[^"]+)""""
       """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
       """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))""""
       """"logonIp":\s*"({src_ip}[a-fA-F:\d.]+)""""
       """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))""""
       """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
       """"domainName"+:\s*"+(-|({web_domain}[^"]+))""""
       """"domainName"+:\s*"+(-|({web_domain}[^"]+))[^}\]]+?userPrincipalName"""
       """"fqdn"+:\s*"+({src_host}[^"]+)""""
       """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}[a-fA-F:\d.]+)"""
       """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}[a-fA-F:\d.]+)"""
       """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
       """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
     
}
```