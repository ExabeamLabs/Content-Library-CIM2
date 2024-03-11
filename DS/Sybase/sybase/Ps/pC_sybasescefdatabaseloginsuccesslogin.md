#### Parser Content
```Java
{
Name = sybase-s-cef-database-login-success-login
Vendor = "Sybase"
Product = "Sybase"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Sybase|ASE Audit|"""
  """msg=Log in"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[A-Fa-f:\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=({user}[^\s]+)"""
  """\Wdhost=({dest_host}[\w\-.]+)"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wcs6=({db_name}.+?)\s+\w+=.+?cs6Label=Database Name"""
  """\Wcs6Label=Database Name.+?cs6=({db_name}.+?)\s+\w+="""
  """\Wcs4=({result}.+?)\s+\w+=.+?cs4Label=Result"""
  """\Wcs4Label=Result.+?cs4=({result}.+?)\s+\w+="""
  """({app}Sybase)"""
]
DupFields = [
  "user->user"
]
ParserVersion = "v1.0.0"


}
```