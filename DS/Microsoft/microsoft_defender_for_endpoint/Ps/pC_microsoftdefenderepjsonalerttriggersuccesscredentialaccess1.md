#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-credentialaccess-1
     Conditions = [ """"category":""", """"CredentialAccess"""", """"title":""", """"incidentId":""",  """"detectionSource":""", """"WindowsDefenderAtp"""", """"threatFamilyName":""" ]
    ParserVersion = "v1.0.0"

json-microsoft-security-events-1 = {
      Vendor = Microsoft
      Product = Microsoft Defender for Endpoint
      TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
      Fields = [
      """"alertId":\s*"({alert_id}[^"]+)"""",
      """"title":\s*"({alert_name}[^"]+)"""",
      """"severity":\s*"({alert_severity}[^"]+)"""",
      """"category":\s*"({alert_type}[^"]+)"""",
      """"description":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]""",
      """"createdDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
      """"firstActivity":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
      """"firstEventTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
      """"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.-]{1,40}\$?))"""",
      """aadUserId[^}\]]+?"accountName":\s*"(-|({full_name}[^"\s]+\s[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.-]{1,40}\$?))"""",
      """"userPrincipalName":\s*"(-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({user}[\w.-]{1,40}\$?)(@[^"]+)?))"""",
      """"userPrincipalName":\s*"({user_upn}[^"]+?)"""",
      """"domainName"+:\s*"+(-|({domain}[^",]+))"""",
      """"domainName"+:\s*"+(-|({domain}[^",]+))[^}\]]+?userPrincipalName""",
      """"deviceDnsName":\s*"+({src_host}[\w.-]+)"""",
      """"status":\s*"({result}[^”]+)"""",
      """"threatFamilyName":\s*"({malware_family}[^"]+)"""",
      """"entityType":\s*"Process"[^\}]+?"fileName":\s*"({process_name}[^"]+)"""",
      """"entityType":\s*"Process"[^\}]+?"processId":\s*"({process_id}[^"]+)"""",
      """"entityType":\s*"File"[^\}]+?"fileName":\s*"({file_name}[^"]+?(\.({file_ext}[^".]+?)?))"""",
      """"entityType":\s*"File"[^\}]+?"filePath":\s*"({file_path}[^"]+)"""",
      """ipAddress\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
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