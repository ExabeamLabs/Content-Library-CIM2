#### Parser Content
```Java
{
Name = pingidentity-pi-json-app-authentication-success-user
  Vendor = Ping Identity
  Product = Ping Identity
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-dd-MM'T'HH:mm:ss.SSSZ"]
  Conditions = [""""source":"PINGID"""",""""type":"user"""",""""status":"SUCCESS"""",""""message":""",""""resources":""",""""result":{"""]
  Fields = [
    """exa_json_path=$.recorded,exa_field_name=time"""
    """exa_json_path=$.actors[0].name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.result.status,exa_field_name=result"""
    """exa_json_path=$.result.message,exa_field_name=additional_info"""
    """exa_json_path=$.resources.devicemodel,exa_field_name=mfa_device"""
    """recorded":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """"actors":\[\{"type":"user","name":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """"devicemodel":"({mfa_device}[^"]+?)""""
    """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"result"*:\{"*status"*:"*({result}[^",]+?)","""
    """"action":"?({action}[^(,|",)+?]+?)(,|",)"""
    """cat=({category}[^\s]+)"""
    """dproc=({process_name}.*?)\s\w+="""
    """requestClientApplication=({app}.*?)\s\w+="""
    """"message":"({additional_info}[^\}]+?)"\}"""
  ]


}
```