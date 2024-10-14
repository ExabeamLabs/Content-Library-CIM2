#### Parser Content
```Java
{
Name = "rangeraudit-ra-json-app-activity-success-enforcer"
ExtractionType = json
Vendor = "RangerAudit"
Product = "RangerAudit"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""RangerAudit"""
"""enforcer"""
"""yarn-acl"""
]
Fields = [
    """evtTime"*:"({time}[^"]+)"""
    """agentHost"*:"({host}[^"]+)"""
    """repo"*:"({app}[^"]+)"""
    """reqUser"*:"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """access"*:"({operation}[^"]+)"""
    """reqData"*:"({additional_info}[^"]+)"""
    """resource"*:"({object}[^"\/]+)"""
    """resType"*:"({resource}[^"]+)"""
    """cliIP"*:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """cluster_name"*:"({dest_host}[^"]+)"""

    """exa_json_path=$.evtTime,exa_field_name=time""",
    """exa_json_path=$.agentHost,exa_field_name=host""",
    """exa_json_path=$.repo,exa_field_name=app""",
    """exa_json_path=$.reqUser,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$""",
    """exa_json_path=$.access,exa_field_name=operation""",
    """exa_json_path=$.reqData,exa_field_name=additional_info""",
    """exa_json_path=$.resource,exa_field_name=object""",
    """exa_json_path=$.resType,exa_field_name=resource""",
    """exa_json_path=$.cliIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.cluster_name,exa_field_name=dest_host"""
]
ParserVersion = "v1.0.0"


}
```