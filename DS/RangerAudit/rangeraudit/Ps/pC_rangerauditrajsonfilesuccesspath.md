#### Parser Content
```Java
{
Name = "rangeraudit-ra-json-file-success-path"
ExtractionType = json
Vendor = "RangerAudit"
Product = "RangerAudit"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
""""RangerAudit""""
"""resType"""
""""path""""
]
Fields = [
    """evtTime"*:"({time}[^"]+)"""
    """agentHost"*:"({host}[^"]+)"""
    """repo"*:"({app}[^"]+)"""
    """reqUser"*:"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """access"*:"({access}[^"]+)"""
    """resource"*:"({file_path}[^"]+)"""
    """action"*:"({action}[^"]+)"""
    """cliIP"*:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """cluster_name"*:"({dest_host}[^"]+)"""

    """exa_json_path=$.evtTime,exa_field_name=time""",
    """exa_json_path=$.agentHost,exa_field_name=host""",
    """exa_json_path=$.repo,exa_field_name=app""",
    """exa_json_path=$.reqUser,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.access,exa_field_name=access""",
    """exa_json_path=$.resource,exa_field_name=file_path""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.cliIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.cluster_name,exa_field_name=dest_host"""
]
ParserVersion = "v1.0.0"


}
```