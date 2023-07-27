#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-asc
Vendor = Microsoft
Product = Microsoft Defender for Cloud
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """CEF:""", """destinationServiceName =Azure""", """cat=security-alert""", """"category":""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":"ASC"""" ]
Fields = [
""""eventDateTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z)"""
"""act=({action}[^\s]+)"""
""""hostStates":\[\{"fqdn":"({host}[\w\-.]+)"""
""""category":"({alert_type}[^"]+)"""
""""logonIp":({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""netBiosName":"(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))|({src_host}[\w\-.]+))"""
"""domainName":"((?i)null|({domain}[^,]+?))\s*""""
""""description":"({additional_info}[^"]+)"""
""""severity":"({alert_severity}[^"]+)"""
""""id":"({alert_id}[^"]+)"""
""""sourceMaterials":\["({malware_url}[^"]+)"""
""""title":"({alert_name}[^"]+)"""
""""userPrincipalName":"((?i)null|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({full_name}[^\s"]+\s+[^"]+)|({user}[\w\.\-]{1,40}\$?)))""""
""""userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^@"]+))?)\\?""""
""""logonLocation":((?i)null|({src_location}[^"]+))"""
""""sourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""+provider"+:"+({provider_name}[^",]+)"""
""""+azureSubscriptionId"+:"+({subscription_id}[^",]+)""",
"""msg=.*?\[({alert_source}[^\]]+)\]:"""
]
DupFields = [ "alert_name->alert_subject" ]
ParserVersion = v1.0.0


}
```