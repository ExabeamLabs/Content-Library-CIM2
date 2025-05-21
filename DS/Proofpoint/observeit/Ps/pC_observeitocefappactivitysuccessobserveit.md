#### Parser Content
```Java
{
Name = "observeit-o-cef-app-activity-success-observeit"
Vendor = "Proofpoint"
Product = "ObserveIT"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|ObserveIT|ObserveIT|"""
]
Fields = [
"""\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)"""
"""\Wcat=(|({operation}.+?))(\s+\w+=|\s*$)"""
"""\Wrt=({time}\d{13})"""
"""({app}ObserveIT)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)"""
"""\Wdvchost=(|({host}.+?))(\s+\w+=|\s*$)"""
"""\WdestinationServiceName =(|({object}.+?))(\s+\w+=|\s*$)"""
"""\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wshost=\(?(|({src_host}[\w\-.]+))\)?(\s+\w+=|\s*$)"""
"""\Wduser=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Wdntdom=(|({domain}.+?))(\s+\w+=|\s*$)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```