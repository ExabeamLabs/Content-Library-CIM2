#### Parser Content
```Java
{
Name = forescout-eyeinspect-json-app-logout-success-clientip
  Vendor = Forescout
  Product = EyeInspect 
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"action":"Logout"""", """"resource":"Operating system Command Center"""", """"clientIP":""", """"user":"""", """"otherInfo":"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.user,exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
    """exa_json_path=$.clientIP,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.otherInfo,exa_field_name=additional_info""",
    """exa_json_path=$.action,exa_field_name=event_name""",
    """exa_json_path=$.resource,exa_field_name=resource"""
  ]
  ParserVersion = "v1.0.0"


}
```