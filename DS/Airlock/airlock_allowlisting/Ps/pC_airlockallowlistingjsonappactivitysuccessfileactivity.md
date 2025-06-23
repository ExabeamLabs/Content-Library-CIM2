#### Parser Content
```Java
{
Name = airlock-allowlisting-json-app-activity-success-fileactivity
  Vendor = Airlock
  Product = Airlock Allowlisting
  TimeFormat = "dd/MM/yyyy HH:mm:ss a"
  ExtractionType = json
  Conditions = [ """"event":"FileActivityMessage"""", """"username":"""", """"datetime":"""",  ]
  Fields = [
    """exa_json_path=$.datetime,exa_field_name=time""",
    """exa_json_path=$.hostname,exa_regex=({host}[\w\-\.]+)"""
    """exa_json_path=$.username,exa_regex=(SYSTEM|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
    """exa_json_path=$.path,exa_field_name=file_dir""",
    """exa_json_path=$.filename,exa_regex=({file_name}[^\"\\\/]+(\.({file_ext}[^\.\"]+)))""",
    """exa_regex=({event_name}FileActivityMessage)""",
    """exa_json_path=$.event,exa_field_name=operation""",
    """exa_json_path=$.sha256,exa_field_name=hash_sha256""",
    """exa_json_path=$.md5,exa_field_name=hash_md5""",
    """exa_json_path=$.parentprocess,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$""",
    """exa_json_path=$.commandline,exa_field_name=process_command_line""",
    """exa_json_path=$.group,exa_field_name=group_name""",
    """exa_json_path=$.execution_type,exa_field_name=event_name"""
  ]
  ParserVersion = "v1.0.0"


}
```