#### Parser Content
```Java
{
Name = "observeit-o-cef-alert-trigger-success-high"
Vendor = "Proofpoint"
Product = "ObserveIT"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|ObserveIT|ObserveIT|"""
"""|ObserveITAlert|"""
]
Fields = [
"""\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)"""
"""\Wcat=(|({operation}.+?))(\s+\w+=|\s*$)"""
"""\Wrt=({time}\w{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})"""
"""\Wrt=({time}\d{13})"""
"""({app}ObserveIT)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)"""
"""\Wdvchost=\(?(|({host}[\w.-]+?))\)?(\s+\w+=|\s*$)"""
"""\Wcs2=(|({os}.+?))(\s+\w+=|\s*$)"""
"""\WdestinationServiceName =(|({object}.+?))(\s+\w+=|\s*$)"""
"""\Wdhost=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wshost=\(?(|({src_host}[\w\-.]+))\)?(\s+\w+=|\s*$)"""
"""\Wduser=(|(?i)n\/a|({user}.+?))(\s+\w+=|\s*$)"""
"""\Wdntdom=(|({domain}.+?))(\s+\w+=|\s*$)"""
"""\WdeviceSeverity=(|({alert_severity}.+?))(\s+\w+=|\s*$)"""
"""\WeventId=(|({alert_id}.+?))(\s+\w+=|\s*$)"""
"""\Wcs5=(|({malware_url}.+?))(\s+\w+=|\s*$)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```