#### Parser Content
```Java
{
Name = microsoft-azuresc-json-alert-trigger-success-geoanomaly
 ParserVersion = v1.0.0
 Vendor = Microsoft
 Product = Microsoft Defender
 ExtractionType = json
 TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ssZ"]
 Conditions = [ """"category":""", """"SQL.DB_GeoAnomaly"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"ASC"""" ]
 Fields = [
     """"securityResources":[\{"resource":"[^"]+\/databases\/({db_name}[^"\/]+)","resourceType":""attacked""""
     """"Someone logged on to your SQL server \'({server_group}[^\']+)\' from an unusual location.""""
     """"id":\s*"({alert_id}[^"]+)"""",
     """"title":\s*"({alert_name}[^"]+?)(\\u200b)?"""",
     """"severity":\s*"({alert_severity}[^"]+)"""",
     """"category":\s*"({alert_type}[^"]+)"""",
     """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]""",
     """"sourceMaterials":\["({additional_info}[^"]+)"""",
     """"eventDateTime":\s*"({time}[^"]+)"""",
     """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
     """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
     """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"userPrincipalName":\s*"(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))"""",
     """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
     """"domainName"+:\s*"+(-|({domain}[^"]+))"""",
     """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName""",
     """"fqdn"+:\s*"+({src_host}[^"]+)"""",
     """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious""",
     """"fileStates":[^]]+?"name":\s*"({file_name}[^."]+([\.\w]+)?)""""
     """"destinationServiceName":"({app}[^"]+)""""
     """"sourceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"Client hostname[\\]*":[\\]*"({src_host}[\w\-\.]+)""",
     """msg=.*?\[({alert_source}[^\]]+)\]:"""   
     """exa_json_path=$.id,exa_field_name=alert_id""",
     """exa_json_path=$.title,exa_field_name=alert_name""",
     """exa_json_path=$.severity,exa_field_name=alert_severity""",
     """exa_json_path=$.category,exa_field_name=alert_type""",
     """exa_json_path=$.description,exa_field_name=additional_info""", 
     """exa_json_path=$.eventDateTime,exa_field_name=time""",
     """exa_json_path=$.userStates[0].accountName,exa_regex=\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
     """exa_json_path=$.userStates[0].logonIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """exa_json_path=$.userStates[0].userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?)""",
     """exa_regex="sourceAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """exa_json_path=$.userStates[0].domainName,exa_field_name=domain""",            
     """exa_json_path=$.userStates[0].userPrincipalName,exa_field_name=user_upn""",
]


}
```