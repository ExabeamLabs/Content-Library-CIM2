#### Parser Content
```Java
{
Name = "icdb-i-cef-app-activity-success-appactivity"
Vendor = "ICDB"
Product = "ICDB"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|ICDB|ICDB|"""
  """requestContext="""
]
Fields = [
  """({app}ICDB)"""
  """CEF:([^\|]*\|){5}({operation}[^\|]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[a-fA-F\d.:]+)"""
  """\Wdvchost=({host}[^=]+?)(\s+\w+=|\s*$)"""
  """\WrequestContext=[^\s=]*?;({target}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wshost=({src_host}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=(({domain}[^=]*?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
  """\Wduid=({object}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wfname=({additional_info}[^=]+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```