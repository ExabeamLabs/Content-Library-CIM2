#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-asc
Vendor = Microsoft
Product = Microsoft Defender
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [ """"status":"""", """"category":""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":"ASC"""" ]
Fields = [
""""eventDateTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}(\.\d+)?Z)"""
"""act=({action}[^\s]+)"""
""""hostStates":\[\{"fqdn":"({host}[\w\-.]+)"""
""""category":"({alert_type}[^"]+)"""
""""logonIp":({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""netBiosName":"(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))|({src_host}[\w\-.]+))"""
"""domainName":"((?i)null|({domain}[^,]+?))\s*""""
""""description":"({additional_info}[^"]+)"""
""""severity":"({alert_severity}[^"]+)"""
""""id":"({alert_id}[^"]+)"""
""""sourceMaterials":\["({malware_url}[^"]+)"""
""""title":"({alert_subject}({alert_name}[^"]+?))(\\u200b)?""""
""""userPrincipalName":"((?i)null|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({full_name}[^\s"]+\s+[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""""
""""userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@"]+))?)\\?""""
""""logonLocation":((?i)null|({src_location}[^"]+))"""
""""sourceAddress":"(00.00.00.00|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?"""
""""+provider"+:"+({provider_name}[^",]+)"""
""""+azureSubscriptionId"+:"+({subscription_id}[^",]+)""",
"""msg=.*?\[({alert_source}[^\]]+)\]:"""
""""status":"({incident_status}[^"]+)""""
]
ParserVersion = v1.0.0


}
```