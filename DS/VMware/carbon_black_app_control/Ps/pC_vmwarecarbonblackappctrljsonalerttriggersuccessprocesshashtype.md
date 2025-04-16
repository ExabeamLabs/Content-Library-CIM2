#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-json-alert-trigger-success-processhashtype
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy hh:mm:ss a","M/d/yyyy h:mm:ss a" ,"yyyy-MM-dd HH:mm:ss"]
  ExtractionType = json
  Conditions = [ """"Bit9Server"""", """"ProcessHashType"""" ]
  Fields = [
    """exa_json_path=$.Timestamp,exa_field_name=time""",
    """exa_json_path=$.Bit9Server,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$.EventType,exa_field_name=alert_type""",
    """exa_json_path=$.EventSubType,exa_field_name=alert_name""",
    """exa_json_path=$.HostName,exa_regex=^(({web_domain}[^\\]+)\\+)?({src_host}[\w\-.]+)$""",
    """exa_json_path=$.HostIP,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
    """exa_json_path=$.Priority,exa_field_name=alert_severity""",
    """exa_json_path=$.ABId,exa_field_name=alert_id""",
    """exa_json_path=$.Message,exa_field_name=additional_info""",
    """exa_json_path=$.PathName,exa_field_name=url""",
    """exa_json_path=$.UserName,exa_regex=^(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_regex=c:\\+users\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]


}
```