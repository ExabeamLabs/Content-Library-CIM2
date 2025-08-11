#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-initialaccess-2
     ExtractionType = json
     Conditions = [ """"category":""", """"InitialAccess"""", """"title":""", """"incidentId":""",  """"detectionSource":""", """"threatFamilyName":""" ]
     ParserVersion = "v1.0.0"

json-microsoft-security-events-1 = {
      Vendor = Microsoft
      Product = Microsoft Defender
      TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
      Fields = [
      """"alertId":\s*"({alert_id}[^"]+)"""",
      """"incidentId":\s*({alert_id}\d+)""",
      """"title":\s*"({alert_name}[^"]+?)(\\u200b)?"""",
      """"severity":\s*"({alert_severity}[^"]+)"""",
      """"category":\s*"({alert_type}[^"]+)"""",
      """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]""",
      """"creationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)""",
      """"createdDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z?)""",
      """"firstActivity":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
      """"firstEventTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
      """"accountName":\s*"((?i:-|SYSTEM)|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({account}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """aadUserId[^}\]]+?"accountName":\s*"((?i:-|SYSTEM)|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """"userPrincipalName":\s*"(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))"""",
      """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
      """"domainName"+:\s*"+((?i:-|NT AUTHORITY)|({domain}[^",]+))"""",
      """"domainName"+:\s*"+((?i:-|NT AUTHORITY)|({domain}[^",]+))[^}\]]+?userPrincipalName""",
      """"deviceDnsName":\s*"+({src_host}[\w.-]+)"""",
      """"status":\s*"({incident_status}[^",]+)"""",
      """"threatFamilyName":\s*"({malware_family}[^"]+)"""",
      """"entityType":\s*"Process"[^\}]+?"fileName":\s*"({process_name}[^"]+)"""",
      """"entityType":\s*"Process"[^\}]+?"processId":\s*"({process_id}[^"]+)"""",
      """"entityType":\s*"File"[^\}]+?"fileName":\s*"({file_name}[^"]+?(\.({file_ext}[^".]+?)?))"""",
      """"entityType":\s*"File"[^\}]+?"filePath":\s*"({file_dir}[^"]+)"""",
      """ipAddress\":\"(00.00.00.00|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\""""
      """"mitreTechniques":\[({technique}[^\]]+)\]"""
      """"evidence".+?"verdict":"({result}[^"]+)"""
      """recipientEmailAddress":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
      """exa_json_path=$.incidentId,exa_field_name=alert_id"""
      """exa_json_path=$.alertId,exa_field_name=alert_id"""
      """exa_json_path=$.title,exa_field_name=alert_name"""
      """exa_json_path=$.severity,exa_field_name=alert_severity"""
      """exa_json_path=$.category,exa_field_name=alert_type"""
      """exa_json_path=$.description,exa_field_name=additional_info"""
      """exa_json_path=$.createdDateTime,exa_field_name=time""",
      """exa_regex="createdDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
      """exa_regex="firstActivity":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,7}?Z)"""
      """exa_regex="firstEventTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)""""
      """exa_regex="accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
      """exa_regex="aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
      """exa_regex="userPrincipalName":\s*"(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))""""
      """exa_regex="userPrincipalName":\s*"({user_upn}[^"]+?)""""
      """exa_regex="domainName":\s*"({domain}[^"]+)""""
      """exa_regex="deviceDnsName":\s*"+({src_host}[\w.-]+)""""
      """exa_json_path=$.status,exa_field_name=incident_status"""
      """exa_json_path=$.threatFamilyName,exa_field_name=malware_family"""
      """exa_regex="ipAddress":\s*"(00.00.00.00|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?"""
      """exa_regex="entityType":\s*"Process"[^\}]+?"fileName":\s*"({process_name}[^"]+)"""",
      """exa_regex="entityType":\s*"Process"[^\}]+?"processId":\s*"({process_id}[^"]+)"""",
      """exa_regex="entityType":\s*"File"[^\}]+?"fileName":\s*"({file_name}[^"]+?(\.({file_ext}[^".]+?)?))"""",
      """exa_regex="entityType":\s*"File"[^\}]+?"filePath":\s*"({file_dir}[^"]+)"""",
      """exa_json_path=$.evidence[:1].recipientEmailAddress,exa_field_name=email_address"""
      """exa_json_path=$.mitreTechniques,exa_field_name=technique"""
      """exa_json_path=$.incidentId,exa_field_name=alert_id"""
      """exa_regex="evidence".+?"verdict":"({result}[^"]+)""""
      ]
 },

microsoft-dns-renew-jp = {
  Vendor = Microsoft
  Fields = [
    """({time}\d\d/\d\d/\d\d,\d\d:\d\d:\d\d),""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+)[\+\-]\d+:\d+\s+({host}[\w\-.]+)\s+\[""",
    """({time}\d+\/\d+\/\d+,\d+:\d+:\d+[\+\-]\d+:\d+)""",
    """<Identifier>({host}[^<]+)<\/Identifier>""",
    """,(DNS.*)?(更新|要求|成功|更新成功)([^,]+)?,({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_host}[\w\-.]+),(|({dest_mac}[^,]+))?,"""
  ]
  DupFields = [ "dest_host->user" 
}
```