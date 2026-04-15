#### Parser Content
```Java
{
Name = pingidentity-pingone-sk4-app-activity-ping
  ParserVersion = v1.0.0
  Vendor = Ping Identity
  Product = PingOne
  ExtractionType = json
  TimeFormat = ["epoch", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-dd-MM'T'HH:mm:ss.SSSZ"]
  Conditions = [ """destinationServiceName =Ping""", """PingOne""", """"source":"""]
  Fields = [
    """cat=({category}[^\s]+)""",
    """end=({time}\d{13})""",
    """dproc=({process_name}[^\s]+)"""
    """flexString2=({result}[^\s]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """suid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """oldFile=({user_agent}.*?)\s\w+=""",
    """msg=({additional_info}.*?)\s\w+=""",
    """fname=({full_name}.*?)\s\w+="""
    """exa_json_path=$.recorded,exa_field_name=time""",
    """exa_json_path=$.action.type,exa_field_name=operation""",
    """exa_json_path=$.result.status,exa_field_name=result""",
    """exa_json_path=$.result.message,exa_field_name=additional_info""",
    """exa_json_path=$.client.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.client.id,exa_field_name=user_agent"""
    """exa_json_path=$..actors[?(@.type == 'user')].name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """exa_json_path=$.actors[0].name,exa_regex=({group_name}[\s\w]+)@directory"""
    """exa_json_path=$.resources[0].name,exa_field_name=resource_name""",
    """exa_json_path=$.resources[0].type,exa_field_name=resource_type""",
    """exa_json_path=$.source,exa_field_name=alert_source"""
  ]


}
```