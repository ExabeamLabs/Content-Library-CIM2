#### Parser Content
```Java
{
Name = "swift-s-cef-app-activity-success-software"
Vendor = "Swift"
Product = "Swift"
TimeFormat = "epoch"
Conditions = [
"""|SWIFT|"""
"""|Alliance Access|"""
"""|Software|"""
"""CEF:"""
]
Fields = [      
    """\srt=({time}\d{13})""",
    """\Wdvc=({host}[A-Fa-f:\d.]+)""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """({app}SWIFT)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({operation}Software)""",
    """msg=({additional_info}.+?)\s*dvchost""",
    """ ({dtz}[^\s]+)"""
    """\Wdvcmac=({dest_mac}[A-Fa-f:\d.]+)\s"""
]
ParserVersion = "v1.0.0"


}
```