#### Parser Content
```Java
{
Name = "attivo-botsink-cef-alert-trigger-success-sshd"
Vendor = "Attivo"
Product = "BOTsink"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Attivo|BOTsink|"""
]
Fields = [
"""CEF:([^\|]*\|){5}({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
"""\Wmsg=(|({additional_info}.+?))(\s+\w+=|\s*$)"""
"""\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)"""
"""\Wrt=({time}\d{13})"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wduser=(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""\Wshostname=(|({src_host}.+?))(\s+\w+=|\s*$)"""
"""\Wsmac=(|({src_mac}.+?))(\s+\w+=|\s*$)"""
"""\Wdhost=(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+?))(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```