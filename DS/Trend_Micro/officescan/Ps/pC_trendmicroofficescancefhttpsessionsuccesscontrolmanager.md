#### Parser Content
```Java
{
Name = trendmicro-officescan-cef-http-session-success-controlmanager
Vendor = Trend Micro
Product = OfficeScan
TimeFormat = "MMM dd yyyy HH:mm:ss zZ"
Conditions = [
  """|Trend Micro|Control Manager|"""
  """|WB:36|"""
]
Fields = [
  """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+[\+\-]\d+:\d+)"""
  """({host}[\w\-.]+)\s+CEF:"""
  """\Wdvchost=({host}[^\s]+)"""
  """\Wdpt=({dest_port}\d+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wcs1=({policy_name}.+?)\s+\w+="""
  """\Wrequest=(-|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)(:\d+)?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s,]*)?))\s+(\w+=|$)"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\WdeviceFacility=({operation}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```