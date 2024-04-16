#### Parser Content
```Java
{
Name = "blackberry-c-json-alert-trigger-success-cylancescore"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
ExtractionType = json
TimeFormat = "M/d/yyyy H:mm:ss a"
Conditions = [
""""Cylance Score""""
""""PUP - """
""""Tenant""""
]
Fields = [
"""exa_json_path=$.['Access Time'],exa_field_name=time"""
"""exa_json_path=$.Date,exa_field_name=time"""
"""exa_json_path=$.['Device Name'],exa_field_name=host"""
"""exa_json_path=$.DeviceName,exa_field_name=host"""
"""exa_json_path=$.Classification,exa_field_name=alert_name"""
"""exa_json_path=$.Classification,exa_field_name=alert_type"""
"""exa_json_path=$.['File Owner'],exa_regex=((N/A)|(({domain}[^\\]+)\\+({user}[\w\.\-]{1,40}\$?)))"""
"""exa_json_path=$.['Cylance Score'],exa_field_name=alert_severity"""
"""exa_json_path=$.['File Path'],exa_regex=({file_dir}([^"\\]|(\\\\)*\\"|\\[^"])+)\\+({file_name}([^"\\]|(\\\\)*\\"|\\[^"])+)"""
"""exa_json_path=$.['File Path'],exa_field_name=file_path"""
"""exa_json_path=$.['File Name'],exa_field_name=file_name"""
"""exa_json_path=$.Description,exa_field_name=alert_name"""
"""exa_regex=({hash_type}MD5)"""
"""exa_regex=({hash_type}SHA256)"""
"""exa_json_path=$.MD5,exa_field_name=old_hash"""
"""exa_json_path=$.SHA256,exa_field_name=old_hash"""
]
DupFields = [
"host->src_host"
"old_hash->new_hash"
]
ParserVersion = "v1.0.0"


}
```