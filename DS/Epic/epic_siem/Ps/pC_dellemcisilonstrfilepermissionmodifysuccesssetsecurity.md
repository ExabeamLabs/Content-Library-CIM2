#### Parser Content
```Java
{
Name = "dell-emcisilon-str-file-permission-modify-success-setsecurity"
Conditions = [
""" Isilon"""
"""|SET_SECURITY|SUCCESS|"""
]
ParserVersion = "v1.0.0"

json-epic-siem = {
    Vendor = Epic
    Product = Epic SIEM
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.E1Mid,exa_field_name=operation""",
    """exa_json_path=$.IP,exa_field_name=src_ip""",
    """exa_regex=EMPid":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\^({full_name}[^\^"]+)\^"""
    """exa_json_path=$.OSUSR,exa_field_name=user""",
    """exa_json_path=$.SOURCE,exa_field_name=log_source""",
    """exa_json_path=$.appname,exa_field_name=app""",
    """exa_json_path=$.procid,exa_field_name=event_id""",
    """exa_json_path=$.severityName,exa_field_name=alert_severity""",
    """exa_json_path=$.structuredData,exa_field_name=additional_info""",
    """exa_json_path=$.Action,exa_field_name=action"""
    json-epic-siem = {
    Vendor = Epic
    Product = Epic SIEM
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.E1Mid,exa_field_name=operation""",
    """exa_json_path=$.IP,exa_field_name=src_ip""",
    """exa_regex=EMPid":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\^({full_name}[^\^"]+)\^"""
    """exa_json_path=$.OSUSR,exa_field_name=user""",
    """exa_json_path=$.SOURCE,exa_field_name=log_source""",
    """exa_json_path=$.appname,exa_field_name=app""",
    """exa_json_path=$.procid,exa_field_name=event_id""",
    """exa_json_path=$.severityName,exa_field_name=alert_severity""",
    """exa_json_path=$.structuredData,exa_field_name=additional_info""",
    """exa_json_path=$.Action,exa_field_name=action"""
    ]
  }
}
```