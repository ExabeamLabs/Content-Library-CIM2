#### Parser Content
```Java
{
Name = "logbinder-sharepoint-cef-file-app-fname"
Vendor = "LOGBinder"
Product = "LOGBinder for SharePoint"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""CEF:"""
"""|LOGbinder|"""
""" request="""
""" filePath="""
""" fname="""
]
Fields = [
"""({host}[\w\-.]+)\s+CEF:"""
"""CEF:([^\|]*\|){5}({access}[^\|]+)"""
"""\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""\Wrequest=({file_dir}.+?)\s+(\w+=|$)"""
"""\Wduser=[^\s=]*?(({domain}[^\\\s\|]+)\\+)?(system|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)"""
"""\WfilePath=(|({file_path}(|({file_dir}[^"]*?))[\\\/]*({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\.\s"]+))?)))\s+(\w+=|$)"""
"""\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
"""({app}LOGbinder)"""
]
ParserVersion = "v1.0.0"


}
```