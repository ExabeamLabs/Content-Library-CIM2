#### Parser Content
```Java
{
Name = "fortinet-firewall-cef-app-activity-appctrl"
Vendor = "Fortinet"
Product = "Fortinet Enterprise Firewall"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Fortinet|Fortigate|"""
"""cn1Label=Duration"""
"""|utm: app-ctrl|"""
]
Fields = [
"""\Wproto=({protocol}\w+)"""
"""\Wact=(|({action}.+?))(\s+\w+=|\s*$)"""
"""\Wrt=({time}\d{13})"""
"""\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wspt=({src_port}\d+)"""
"""\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdpt=({dest_port}\d+)"""
"""\WdestinationServiceName =(|({service_name}.+?))(\s+\w+=|\s*$)"""
"""\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)"""
"""\Wcat=({event_subtype}.+?)(\s+\w+=|\s*$)"""
"""\Wapp\\?=\"({app}[^\"]+)\""""
"""\Wmsg=({additional_info}.+?),?(\s+\w+=|\s*$)""",
"""\Wtz="?({tz}[+-]\d+)"""
]
ParserVersion = "v1.0.0"


}
```