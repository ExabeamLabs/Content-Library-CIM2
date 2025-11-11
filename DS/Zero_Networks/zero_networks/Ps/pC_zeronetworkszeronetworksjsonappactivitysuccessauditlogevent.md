#### Parser Content
```Java
{
Name = "zeronetworks-zeronetworks-json-app-activity-success-auditlogevent"
  Vendor = "Zero Networks"
  Product = "Zero Networks"
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"auditType":""" ,""""enforcementSource":""" , """"id":"""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.parentObjectId,exa_field_name=object_id"""
    """exa_json_path=$.details,exa_regex=localEntityNames\\":[^\}]+"name\\":\\"({dest_host}[^"\\]+)\\?""""
    """exa_json_path=$.details,exa_regex=remoteEntityNames\\":[^\}]+"name\\":\\"({src_host}[^"\\]+)\\?""""
    """exa_json_path=$.destinationEntitiesList,exa_regex="id":"({object_id}[^"]+)"""
    """exa_json_path=$.auditType,exa_field_name=audit_id"""
    """exa_json_path=$.userRole,exa_field_name=role_id"""
    """exa_json_path=$.enforcementSource,exa_field_name=result_code"""
    """exa_json_path=$.details,exa_regex=description\\?":\\?"({description}[^\\"]+)\\?","""
    """exa_json_path=$.performedBy,exa_regex="name":"(((?i)NT AUTHORITY|NT SERVICE|({domain}[^\\]+))[\\]+)?(local service|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({user}[\w\.\-]{1,40}\$?))""""
    """exa_json_path=$.performedBy,exa_regex="name":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "operation->access" ]
  ParserVersion = "v1.0.0"


}
```