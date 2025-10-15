#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-json-app-activity-success-actor"
  Vendor = "VMware"
  Product = "Carbon Black EDR"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ" 
  ExtractionType = json
  Conditions = [ """"actor":"""", """"description":"""", """"actor_ip":"""" ]
  Fields = [
    """exa_json_path=$.create_time,exa_field_name=time"""
    """exa_json_path=$.actor,exa_regex=(?:(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s"]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({=user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.description,exa_field_name=event_name"""
    """exa_json_path=$.actor_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""   
    """exa_json_path=$.org_key,exa_field_name=primary_key"""
  ]
  ParserVersion = "v1.0.0"


}
```