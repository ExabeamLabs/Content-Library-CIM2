#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-share-access-5145"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft|Microsoft Windows|"""
  """|A network share object was checked to see whether client can be granted desired access.|"""
]
Fields = [
  """({event_name}A network share object was checked to see whether client can be granted desired access)""",
  """({event_code}5145)""",
  """\Wrt=({time}\d{13})""",
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """\Wdhost=({dest_host}[\w\-.]+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wdvchost=({host}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """\Wdntdom=({domain}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wduser=({user}[\w\.\-]{1,40}\$?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wduid=({login_id}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\WcategoryOutcome=\/?({result}\w+)""",
  """\W\ad\.ShareName =(?:\\+\*\\+)?({share_name}.+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wcs1=.*?({access}SYNCHRONIZE|Execute|Traverse|Read|READ).*?(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wcs1=.*?({access}WRITE_DAC|WRITE_OWNER|WriteAttributes|WriteEA).*?(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wcs1=.*?({access}WriteData|AppendData).*?(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wcs1=.*?({access}delete|Delete).*?(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wad\.ShareLocalPath=(?:[\\\?]+)?(?:\s*|({share_path}({d_parent}.*?)({d_name}[^\\]+?))(\\+)?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wad\.RelativeTargetName =(({file_dir}.*?)({file_name}[^\\:]+?(\.({file_ext}[^\\.]+?))?))(\s+(\w+|\w+\.\w+)=|\s*$)""",
  """\Wad\.ObjectType=({file_type}\w+)"""
  """Source Port(=|:)\s*({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```