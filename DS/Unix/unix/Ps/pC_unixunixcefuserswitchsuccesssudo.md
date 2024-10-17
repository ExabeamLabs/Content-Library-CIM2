#### Parser Content
```Java
{
Name = "unix-unix-cef-user-switch-success-sudo"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Unix|Unix|"""
"""; COMMAND"""
""" deviceProcessName =sudo """
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\S+)(\s+\w+=|\s*$)"""
"""\sdvchost=({host}\S+)(\s+\w+=|\s*$)"""
"""\sdhost=({dest_host}\S+)(\s+\w+=|\s*$)"""
"""\sdst=({dest_ip}\S+)(\s+\w+=|\s*$)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
"""\ssuid=({user_uid}.+?)(\s+\w+=|\s*$)"""
"""\sduser=({account}.+?)(\s+\w+=|\s*$)"""
"""({event_code}sudo)"""
]
DupFields = [
"event_code->process_name"
]
ParserVersion = "v1.0.0"


}
```