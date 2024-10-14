#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-authentication-fail-unsuccessattempt
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"source":"PINGID"""", """"type":"user"""", """"status":"UNSUCCESSFUL_ATTEMPT"""",""""message":""",""""resources":""",""""result":{"""]
  Fields = [
    """exa_json_path=$.recorded,exa_field_name=time"""
    """exa_json_path=$.actors[0].name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.result.status,exa_field_name=result"""
    """exa_json_path=$.result.message,exa_field_name=additional_info"""
  ]


}
```