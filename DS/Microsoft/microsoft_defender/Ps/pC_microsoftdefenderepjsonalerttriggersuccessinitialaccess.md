#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-initialaccess
  ExtractionType = json
  Product = Microsoft Defender
  ParserVersion = v1.0.0
  Conditions = [ """"category":""", """"InitialAccess"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"Microsoft Defender ATP"""" ]

json-microsoft-security-events = {
     Vendor = Microsoft
     ExtractionType = json
     TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSZ", "yyyy-MM-dd'T'HH:mm:ss.SZ"]
     Fields = [
      """"id":\s*"({alert_id}[^"]+)""""
       """"title":\s*"({alert_subject}({alert_name}[^"]+?))(\\u200b)?""""
       """"severity":\s*"({alert_severity}[^"]+)""""
       """"category":\s*"({alert_type}[^"]+)""""
       """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]"""
       """"sourceMaterials":\["({additional_info}[^"]+)"""",
       """"eventDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)""""
       """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"<]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|([^\."]+\.[^"]+)|({account}[\w\.\-\!\#\^\~]{1,40}\$?))("|\s+<)"""
       """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"<]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|([^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))("|\s+<)"""
       """"logonIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
       """"userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))""""
       """"userPrincipalName":\s*"({user_upn}[^"]+?)""""
       """"domainName"+:\s*"+(-|({domain}[^"]+))""""
       """"domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
       """"fqdn"+:\s*"+({src_host}[\w\-\.]+)"""
       """"hostStates":\[[^\]]*"netBiosName":"({src_host}[^"]+)"""
       """"+hostStates"+:[^}\]]+?privateIpAddress"+:\s*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
       """"+hostStates"+:[^}\]]+?publicIpAddress"+:\s*"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
       """"description":\s*"An actor on\s*({src_host}\S+)\s*performed suspicious"""
       """"fileStates":[^]]+?"name":\s*"(({file_dir}[^"]+)[\\\/])?({file_name}[^."]+(\.({file_ext}[\w]+))?)""""
       """"destinationServiceName":"({app}[^"]+)""""
       """"status":"({incident_status}[^"]+)"""",
       """"logonLocation"+:\s*"+({location}[^"]+)""""
       """"incidentId":\s*"({alert_id}\d+)"""
      """"mitreTechniques":\[({technique}[^\]]+)\]"""
      """"evidence".+?"verdict":"({result}[^"]+)"""
       """exa_json_path=$.id,exa_field_name=alert_id""",
       """exa_json_path=$.title,exa_field_name=alert_name""",
       """exa_json_path=$.title,exa_field_name=alert_subject""",
       """exa_json_path=$.severity,exa_field_name=alert_severity""",
       """exa_json_path=$.category,exa_field_name=alert_type""",
       """exa_json_path=$.sourceMaterials,exa_field_name=additional_info""",
       """exa_json_path=$.description,exa_field_name=additional_info""",
       """exa_json_path=$.eventDateTime,exa_field_name=time""",
       """exa_json_path=$.userStates[:1].accountName,exa_regex=(-|({full_name}[^"\s]+\s[^"<]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|([^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
       """exa_json_path=$.userStates,exa_regex=aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"<]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|([^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))("|\s+<)""",
       """exa_json_path=$.userStates[:1].logonIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """exa_json_path=$.userStates[:1].userPrincipalName,exa_regex=(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))""",
       """exa_json_path=$.userStates[:1].userPrincipalName,exa_field_name=user_upn""",
       """exa_json_path=$.userStates[:1].domainName,exa_field_name=domain""",
       """exa_json_path=$.hostStates[:1].fqdn,exa_field_name=src_host""",
       """exa_json_path=$.hostStates[:1].privateIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """exa_json_path=$.hostStates[:1].publicIpAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """exa_regex="hostStates":\[[^\]]*"netBiosName":"({src_host}[^"]+)"""
       """exa_json_path=$.description,exa_regex=An actor on\s*({src_host}\S+)\s*performed suspicious""",
       """exa_json_path=$.fileStates[:1].name,exa_regex=(({file_dir}[^"]+)[\\\/])?({file_name}[^."]+(\.({file_ext}[\w]+))?)""",
       """exa_json_path=$.status,exa_field_name=incident_status""",
       """exa_json_path=$.logonLocation,exa_field_name=location"""
       """exa_regex="domainName"+:\s*"+(-|({domain}[^"]+))[^}\]]+?userPrincipalName"""
       """exa_json_path=$.mitreTechniques,exa_field_name=technique"""
       """exa_json_path=$.incidentId,exa_field_name=alert_id"""
       """exa_regex="evidence".+?"verdict":"({result}[^"]+)""""
     
}
```