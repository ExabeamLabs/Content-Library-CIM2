#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-alert-trigger-success-threatexchange"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|CarbonBlack|Response|"""
"""feed.ingress.hit.process"""
]
Fields = [
"""({host}[\w.\-]+):\s+CEF:([^\|]*\|){5}({alert_name}[^\|]+)"""
"""\Wend=({time}\d{13})"""
"""\Wmsg=(|({alert_type}.+?))(\s+\w+=|\s*$)"""
"""\Wsuser=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WdeviceProcessName =({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)"""
"""\Wrequest=(|({malware_url}.+?))(\s+\w+=|\s*$)"""
"""\WrequestUrlPort=({dest_port}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```