#### Parser Content
```Java
{
Name = microsoft-mcas-json-alert-trigger-success-download
  Product = Microsoft CAS
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"MCAS_ALERT_ANUBIS_DETECTION_REPEATED_ACTIVITY_DOWNLOAD"""", """vendor":"Microsoft"""", """"sourcetype":"GraphSecurityAlert"""", """provider":"MCAS"""" ]

defender-atp-security-alert-events = {
    Vendor = Microsoft
    TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
    Fields = [
      """"(timestamp|firstActivityDateTime)":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)"""",
      """"hostname":"({host}[^"]+)"""",
      """"severity":"({alert_severity}[^"]+)"""",
      """(privateIpAddress|ipAddress)":"(00.00.00.00|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
      """publicIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"title":"({alert_name}[^"]+)"""",
      """"category":"({alert_type}[^"]+)"""",
      """"description":"({additional_info}[^\n]+?)\s*","""",
      """userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """accountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """domainName":"({domain}[^"]+)""",
      """exa_json_path=$.firstActivityDateTime,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)""",
      """exa_json_path=$.timestamp,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
      """exa_json_path=$.severity,exa_field_name=alert_severity""",
      """exa_regex=privateIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """exa_regex=publicIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """exa_json_path=$.category,exa_field_name=alert_type""",
      """exa_json_path=$.title,exa_field_name=alert_name""",
      """exa_json_path=$.description,exa_field_name=additional_info""",
      """exa_regex=userPrincipalName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """exa_regex=accountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """exa_regex=domainName":"({domain}[^"]+)"""
    
}
```