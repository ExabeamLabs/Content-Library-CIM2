#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-graphdirectoryauditlogs
 ParserVersion = v1.0.0
 Vendor = Microsoft
 Product = Microsoft 365
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"destinationServiceName":"Office 365"""", """"dproc":"Graph Directory Audit logs"""", """"activityDisplayName":""" ]
 Fields = [
   """"activityDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
   """"activityDisplayName":"({operation}[^"]+)""",
   """"userPrincipalName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[^"]+))"""",
   """"category":"({category}[^"]+)""",
   """"destinationServiceName":"({app}[^"]+)""",
   """"result":"({result}[^"]+)""",
   """"resultReason":"({result_reason}[^"]+)""",
   """"value":"({user_agent}[^"]+)","key":"User-Agent"""",
   """"dproc":"({dproc}[^"]+)""",
   """"operationType":"({operation_type}[^"]+)"""",   
   """"loggedByService":"({service_name}[^"]+)""""
 ]


}
```