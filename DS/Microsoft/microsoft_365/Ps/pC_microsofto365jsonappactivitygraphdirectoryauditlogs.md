#### Parser Content
```Java
{
Name = microsoft-o365-json-app-activity-graphdirectoryauditlogs
 ExtractionType = json
 ParserVersion = v1.0.0
 Vendor = Microsoft
 Product = Microsoft 365
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
 Conditions = [ """"destinationServiceName":"Office 365"""", """"dproc":"Graph Directory Audit logs"""", """"activityDisplayName":""" ]
 Fields = [
   """exa_json_path=$.activityDisplayName,exa_field_name=operation"""
   """exa_json_path=$.activityDateTime,exa_field_name=time"""
   """exa_json_path=$.targetResources..userPrincipalName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
   """exa_json_path=$.category,exa_field_name=category"""
   """exa_json_path=$.destinationServiceName,exa_field_name=app"""
   """exa_json_path=$.result,exa_field_name=result"""
   """exa_json_path=$.resultReason,exa_field_name=result_reason"""
   """exa_regex="value":"({user_agent}[^"]+)","key":"User-Agent""""
   """exa_json_path=$.dproc,exa_field_name=dproc"""
   """exa_json_path=$.operationType,exa_field_name=operation_type"""
   """exa_json_path=$.loggedByService,exa_field_name=service_name"""
 ]


}
```