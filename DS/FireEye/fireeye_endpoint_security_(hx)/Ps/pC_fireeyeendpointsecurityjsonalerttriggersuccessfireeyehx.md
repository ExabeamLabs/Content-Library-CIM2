#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-json-alert-trigger-success-fireeyehx
  Vendor = FireEye
  Product = FireEye Endpoint Security (HX)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"FireEyeHX"""", """"HX"""", """"malwarePath":"""", """"malwareMD5":"""" ]
  Fields = [
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_json_path=$.deviceIP,exa_regex=^({host}[A-Fa-f:\d.]+)$""",
    """exa_json_path=$.deviceHostname,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.srcIP,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.malwarePath,exa_field_name=malware_url""",
    """exa_json_path=$.userID,exa_regex=^(({domain}[^"\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.srcOS,exa_field_name=os""",
    """exa_json_path=$.process,exa_field_name=alert_name""",
    """exa_json_path=$.log_type,exa_field_name=alert_type""",
    """exa_json_path=$.srcHostname,exa_regex=^({src_host}[\w\-.]+)$""",
    """exa_json_path=$.malwareMD5,exa_field_name=hash_md5""",
    """exa_json_path=$.deviceSensor,exa_field_name=sensor"""
  ]
  ParserVersion = "v1.0.0"


}
```