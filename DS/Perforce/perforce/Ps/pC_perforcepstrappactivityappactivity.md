#### Parser Content
```Java
{
Name = "perforce-p-str-app-activity-appactivity"
Vendor = "Perforce"
Product = "Perforce"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
  """<Perforce Condition>"""
]
Fields = [
  """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)"""
  """\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d\s({user}[\w\.\-]{1,40}\$?)"""
  """\d\d:\d\d:\d\d\s[^@]+@({additional_info}[^\s]+)"""
  """\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\/"""
  """\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
  """\/\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\s({operation}.+?)\s\/\/"""
  """\s({object}\/\/[^\/]+\/[^\/]+)"""
  """\s\/\/([^\/]+\/){2}({resource}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```