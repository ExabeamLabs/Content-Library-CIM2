#### Parser Content
```Java
{
Name = oracle-pc-json-app-activity-success-adminaccountcreatesuccess
  ParserVersion = "v1.0.0"
  Conditions = [ """"adminResourceType":"""", """"serviceName":"Admin"""", """"eventId":"admin.accountmgmtinfo.create.success"""" ]

oracle-public-cloud-events = {
    Vendor = Oracle
    Product = Oracle Public Cloud
    ExtractionType = json
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ssZ"]
    Fields = [
          """exa_json_path=$..created,exa_field_name=time"""
          """exa_json_path=$..timestamp,exa_field_name=time""",
          """exa_json_path=$..actorName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""


          """exa_json_path=$..ssoPlatform,exa_field_name=os""",
          """exa_json_path=$..idcsLastModifiedBy.display,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^,"]+,[^"]+))""",
          """exa_json_path=$..eventId,exa_field_name=event_name""",
          """exa_json_path=$..ssoApplicationName,exa_field_name=app""",
          """exa_json_path=$..message,exa_field_name=additional_info""",
          """exa_json_path=$..serviceName,exa_field_name=service_name""",
          """exa_json_path=$..clientIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
          """exa_json_path=$..actorType,exa_field_name=user_type"""
          """exa_json_path=$..ssoUserAgent,exa_field_name=user_agent"""
          """exa_json_path=$..resourceType,exa_field_name=resource_type"""
          """exa_json_path=$..appmgmtAppDisplayName,exa_field_name=app"""
          """exa_json_path=$..actorId,exa_field_name=user_id"""
          """exa_json_path=$..clientName,exa_field_name=src_host"""
          """exa_json_path=$..appID,exa_field_name=app_id"""
    
}
```