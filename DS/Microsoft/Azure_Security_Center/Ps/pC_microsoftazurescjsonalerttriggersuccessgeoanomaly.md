#### Parser Content
```Java
{
Name = microsoft-azuresc-json-alert-trigger-success-geoanomaly
 ParserVersion = v1.0.0
 Vendor = Microsoft
 Product = Azure Security Center
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"category":""", """"SQL.DB_GeoAnomaly"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"ASC"""" ]
 Fields = [
     """"securityResources":[\{"resource":"[^"]+\/databases\/({db_name}[^"\/]+)","resourceType":""attacked""""
     """"Someone logged on to your SQL server \'({server_group}[^\']+)\' from an unusual location.""""
     """"id":\s*"({alert_id}[^"]+)"""",
     """"title":\s*"({alert_name}[^"]+)"""",
     """"severity":\s*"({alert_severity}[^"]+)"""",
     """"category":\s*"({alert_type}[^"]+)"""",
     """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]""",
     """"eventDateTime":\s*"({time}[^"]+)"""",
     """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))"""",
     """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}[^"@]+@[^"]+)|({user}[^\s"]+))"""",
     """"logonIp":\s*"({src_ip}[a-fA-F:\d.]+)"""",
     """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))"""",
     """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
     """"domainName"+:\s*"+(-|({domain}[^"]+))"""",
     """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName""",
     """"fqdn"+:\s*"+({src_host}[^"]+)"""",
     """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}[a-fA-F:\d.]+)""",
     """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}[a-fA-F:\d.]+)""",
     """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious""",
     """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
     """"sourceAddress":\s*"({src_ip}[a-fA-F:\d.]+)"""" 
]


}
```