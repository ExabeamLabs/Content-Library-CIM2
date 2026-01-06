#### Parser Content
```Java
{
Name = trendmicro-vone-json-app-activity-success-audit
  Vendor = Trend Micro
  Product = Vision One
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"loggedUser":""", """"loggedRole":""", """"category":""", """"activity":""", """"details":""" ]
  Fields = [
    """exa_json_path=$.loggedDateTime,exa_field_name=time""",
    """exa_json_path=$.Time,exa_field_name=time""",
    """exa_json_path=$.loggedUser,exa_field_name=full_name""",
    """exa_json_path=$.activity,exa_field_name=event_name""",
    """exa_json_path=$.activity,exa_field_name=operation""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$.result,exa_field_name=result""",
    """exa_json_path=$.loggedRole,exa_field_name=role""",
    """exa_json_path=$.details,exa_field_name=additional_info""",
    """exa_json_path=$..user,exa_regex=((({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$..email,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
    """exa_json_path=$..cltIPAddr,exa_regex=({src_ip}((([0-9a-fA-F]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.){3}(25[0-5]|(2[0-4]|1\d|[0-9]|)\d)))(:({src_port}\d+))?""",
    """exa_json_path=$..devName,exa_regex=({src_host}[\w.-]+)""",
    """exa_json_path=$..deviceId,exa_field_name=device_id""",
    """"loggedDateTime":"({time}[^"]+)"""",
    """"Time":"({time}[^"]+)"""",
    """"loggedUser":"({full_name}[^"]+)"""",
    """"activity":"({operation}({event_name}[^"]+))"""",
    """"category":"({category}[^"]+)"""",
    """"result":"({result}[^"]+)"""",
    """"loggedRole":"({role}[^"]+)"""",
    """"details":\{({additional_info}[^=]+?)\}""",
    """"user":"((({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"email":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
    """"cltIPAddr":"({src_ip}((([0-9a-fA-F]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.){3}(25[0-5]|(2[0-4]|1\d|[0-9]|)\d)))(:({src_port}\d+))?""",
    """"devName":"({src_host}[\w.-]+)""",
    """"deviceId":"({device_id}[^"]+)""""
  ]


}
```