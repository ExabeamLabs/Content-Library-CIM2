#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-share-access-5145-4"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""A network share object was checked to see whether client can be granted desired access"""
"""Account Name:"""
"""TimeGenerated="""
"""Computer"""
]
Fields = [
"""({event_name}A network share object was checked to see whether client can be granted desired access)"""
"""({event_code}5145)"""
"""Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*({dest_host}({host}[\w\.-]+))(\s|,|\"|</Computer>|$)"""
"""\sTimeGenerated=({time}\d{10})"""
"""Logon ID:\s*((?-i)\\+[rnt])*({login_id}\S+?)((?-i)\\+[rnt])*\s*Network Information:"""
"""Account Name:\s*((?-i)\\+[rnt])*({user}[\w\.\-\!\#\^\~]{1,40}\$?)((?-i)\\+[rnt])*\s*Account Domain:"""
"""Account Domain:\s*((?-i)\\+[rnt])*({domain}\S+?)((?-i)\\+[rnt])*\s*Logon ID:"""
"""Object Type:\s*((?-i)\\+[rnt])*({file_type}.+?)((?-i)\\+[rnt])*\s*Source Address:"""
"""Source Address:\s*((?-i)\\+[rnt])*(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)((?-i)\\+[rnt])*\s*Source Port:"""
"""Share Name:\s*((?-i)\\+[rnt])*(?:[\\\*]+)?({share_name}.+?)((?-i)\\+[rnt])*\s*Share Path:"""
"""Share Path:\s*((?-i)\\+[rnt])*(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+?)\\)?(|({d_name}[^\\]*?)))\\?)((?-i)\\+[rnt])*\s*Relative Target Name:"""
"""Relative Target Name:\s*((?-i)\\+[rnt])*\\?(?:\s*|(?:({file_dir}.+?)\\)?(|({file_name}[^\\:\/]+?(?:\.({file_ext}[^\.]+?))?))(?:\\HEAD|:.+?|\\|\s|((?-i)\\+[rnt])*)\s*)Access Request Information:"""
"""Accesses:.*({access}SYNCHRONIZE|Execute|Traverse|Read|READ|WRITE_DAC|WRITE_OWNER|WriteAttributes|WriteEA|WriteData|AppendData|delete|Delete).*Access Check Results:"""
"""Access Check Results:\s*({result}-)\s"""
"""Access Check Results:.*({result}Granted|Denied)\s+by"""
"""Source Port(=|:)\s*({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```