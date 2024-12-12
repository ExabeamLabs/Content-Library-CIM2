#### Parser Content
```Java
{
Name = microsoft-azure-sk4-alert-trigger-success-aatp
Vendor = Microsoft
Product = Azure ATP
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ParserVersion = "v1.0.0"
Conditions = [ """CEF:""", """cat=security-alert""", """"category":""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":"Azure Advanced Threat Protection""" ]
Fields = [
  """"eventDateTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})\.\d{1,7}Z"""
  """act=({action}[^\s]+)"""
  """"hostStates":\[\{"fqdn":"({host}[\w\-.]+)"""
  """"category":"({alert_type}[^"]+)"""
  """"logonIp":({src_ip}[A-fa-f\d:.]+)"""
  """"netBiosName":"(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))|({src_host}[\w\-.]+))"""
  """domainName":((?i)null|({domain}"[^,]+))"""
  """"description":"({additional_info}[^"]+)"""
  """"severity":"({alert_severity}[^"]+)"""
  """"id":"({alert_id}[^"]+)"""
  """"sourceMaterials":\["({malware_url}[^"]+)"""
  """"title":"({alert_name}[^"]+)"""
  """"userPrincipalName":"((?i)null|(({full_name}[^\s"]+\s+[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  """"userPrincipalName":"((?i)null|({email_user}[^\@"]+\@([^\."]+\.)*\w+))"""
  """"logonLocation":((?i)null|({src_location}[^"]+))"""
  """"status":"({incident_status}[^",]+)"""
]


}
```