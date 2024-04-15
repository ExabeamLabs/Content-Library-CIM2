#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-share-access-success-5140-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|Snare|"""
"""A network share object was accessed"""
"""Microsoft-Windows-Security-Auditing:5140|"""
]
Fields = [
"""({event_name}A network share object was accessed)"""
"""({event_code}5140)"""
"""\Wrt=({time}\d{13})"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdhost=({dest_host}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""\Wdvchost=({host}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""\Wduser=({user}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""\Wduid=({login_id}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""\WfilePath=(?:\\+\*\\+)?({share_name}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""({access}Read)"""
"""\Wad\.ShareLocalPath=(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)(\s+(\w+|\w+\.\w+)=|\s*$)"""
"""\WfileType=({file_type}\w+)"""
"""\WcategoryOutcome=\/?({result}.+?)\s+(\w+=|$)"""
"""\WObject Type:\s*({file_type}.+?)\s+Source Address:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\WShare Name:\s*({share_name}.+?)\s+Share Path:"""
"""\WShare Path:\s*(|({share_path}({d_parent}.*?[\\\/]+)?(|({d_name}[^\\]+?))))\s+Access Request Information:"""
]
ParserVersion = "v1.0.0"


}
```