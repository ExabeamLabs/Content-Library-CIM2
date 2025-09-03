#### Parser Content
```Java
{
Name = "swift-s-cef-app-login-success-signon"
Vendor = "Swift"
Product = "Swift"
TimeFormat = "epoch"
Conditions = [
"""|SWIFT|"""
"""|Successful signon|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\Wdvc=({host}[A-Fa-f:\d.]+)"""
"""\Wdvchost=({host}[\w\-.]+)"""
"""suid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""({app}SWIFT)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""msg=([^:]+):\s*({full_name}[^,=]+),"""
"""({operation}(({result}Successful)) signon)"""
"""msg=({additional_info}.+?)Operator Profiles:\s*({profiles}.+?)(\s*\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```