#### Parser Content
```Java
{
Name = "dell-oim-cef-user-password-modify-success-forcechange"
Vendor = "Dell"
Product = "One Identity Manager"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|SCB|PAM|"""
"""|Force Change|"""
]
Fields = [
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
"""\sdhost=({dest_host}.+?)(\s+\w+=|\s*$)"""
"""\sduser=({dest_user}.+?)(\s+\w+=|\s*$)"""
"""\sdvc=({host}.+?)(\s+\w+=|\s*$)"""
"""\sdvchost=({host}.+?)(\s+\w+=|\s*$)"""
"""\srt=({time}\d{13})"""
"""\sOtherInfo:\s*({result}.+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```