#### Parser Content
```Java
{
Name = cybereason-cr-json-alert-trigger-success-affectedusers
  Vendor = Cybereason
  Product = Cybereason
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"hasSuspicions": true""", """"hasMalops": true""", """"affectedMachines"""", """"affectedUsers"""" ]
  Fields = [
    """exa_json_path=$.creationTime,exa_field_name=time"""
    """exa_json_path=$.detectionType,exa_field_name=alert_type"""
    """exa_regex="affectedMachines":\s*\{[^\}]+?"elementType":\s*"Machine"[^\}]+?"name":\s*"({dest_host}[^"]+)""""
    """exa_regex="affectedUsers":\s*\{[^\}]+"elementType":\s*"User"[^\}]+"name":\s*"((nt service|nt instans|({domain}[^\\"]+))\\+)?(network service|system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """exa_json_path=$.message,exa_field_name=additional_info"""
    """exa_json_path=$..suspects..elementDisplayName.values[0],exa_field_name=additional_info"""
    """exa_json_path=$.malopActivityTypes,exa_field_name=threat_category"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
  ]
  DupFields = ["alert_type->alert_name"]


}
```