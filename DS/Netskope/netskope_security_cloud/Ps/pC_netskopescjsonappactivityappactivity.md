#### Parser Content
```Java
{
Name = netskope-sc-json-app-activity-appactivity
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"nsdeviceuid":""", """"event": """, """"status": """ ]
  Fields = [
    """exa_json_path=$.status,exa_field_name=result"""
# device_classification_status is removed
# user_groups is removed
    """exa_json_path=$.username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""
# user_source is removed
    """exa_json_path=$.device_id,exa_field_name=device_id"""
    """exa_json_path=$.client_version,exa_field_name=client_version"""
    """exa_json_path=$.os,exa_field_name=os"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.actor,exa_regex=(System|User|({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.os_version,exa_field_name=os_version"""
# internal_id is removed
    """exa_json_path=$.device_model,exa_field_name=device_model"""
    """exa_json_path=$.hostname,exa_field_name=host"""
# nsdeviceuid is removed
    """exa_json_path=$.event,exa_field_name=event_name"""
# user_key is removed
# npa_status is removed
  ]


}
```