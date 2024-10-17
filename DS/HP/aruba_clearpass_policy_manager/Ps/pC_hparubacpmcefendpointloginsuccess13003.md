#### Parser Content
```Java
{
Name = "hp-arubacpm-cef-endpoint-login-success-13003"
Vendor = "HP"
Product = "Aruba ClearPass Policy Manager"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|Aruba Networks|ClearPass|"""
"""|13003|"""
]
Fields = [
"""\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\Wdvc=({host}.+?)(\s+\w+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wduser=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
"""\Wdmac=({dest_mac}.+?)(\s+\w+=|\s*$)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\w+=|\s*$)"""
"""\WdestinationServiceName =({network}.+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```