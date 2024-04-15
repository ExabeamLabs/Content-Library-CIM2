#### Parser Content
```Java
{
Name = "delinea-ss-cef-app-activity-success-thycotic"
Vendor = "Delinea"
Product = "Thycotic Software Secret Server"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|Thycotic Software|Secret Server|"""
"""Item Name:"""
]
Fields = [
"""\d{2}:\d{2}:\d{2} ({host}[\w\-.]+) CEF:"""
"""\srt=({time}\d+)"""
"""\srt=({time}\w+ \d{2} \d{4} \d{2}:\d{2}:\d{2})"""
"""\sdvc=({host}[^\s]+)"""
"""\sdvchost=({host}[^\s]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\s\w+="""
"""\ssuser=(({domain}[^\\=]+)(\\)+)?({user}[^=]+?)\s+\w+="""
"""({app}Thycotic Software)"""
"""\sfname=({object}[^=]+?)\s+\w+="""
"""\sContainer Name:\s*({resource}[^=]+?)\s*(?:\([^\)]*?\))?\s+(\w+=|\w+:|$)"""
"""Action: \[({operation}[^\]]+)\]"""
"""\sfileType=({additional_info}[^=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```