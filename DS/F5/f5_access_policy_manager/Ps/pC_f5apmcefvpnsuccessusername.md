#### Parser Content
```Java
{
Name = "f5-apm-cef-vpn-success-username"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "epoch"
Conditions = [
"""|F5|APM|"""
"""Username|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sduser=({user}[\w\.\-]{1,40}\$?)(?:\s+[\w.]+=|\s*$)"""
"""\scs4=({session_id}.+?)(?:\s+[\w.]+=|\s*$)"""
"""\sdvc=({host}[a-fA-F\d.:]+)"""
"""\sdvchost=({host}.+?)(?:\s+[\w.]+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```