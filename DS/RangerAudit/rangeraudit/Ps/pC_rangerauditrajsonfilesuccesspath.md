#### Parser Content
```Java
{
Name = "rangeraudit-ra-json-file-success-path"
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
"""reqUser"*:"({user}[^"]+)"""
"""access"*:"({access}[^"]+)"""
"""resource"*:"({file_path}[^"]+)"""
"""action"*:"({action}[^"]+)"""
"""cliIP"*:"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""cluster_name"*:"({dest_host}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```