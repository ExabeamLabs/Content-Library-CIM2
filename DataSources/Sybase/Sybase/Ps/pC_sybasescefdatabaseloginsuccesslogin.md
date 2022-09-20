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
  """\Wrt=({time}\d+)"""
  """\Wdvc=({host}[A-Fa-f:\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wshost=({src_host}[\w\-.]+)"""
  """\Wsrc=({src_ip}[A-Fa-f:\d.]+)"""
  """\Wsuser=({user}[^\s]+)"""
  """\Wdhost=({dest_host}[\w\-.]+)"""
  """\Wdst=({dest_ip}[A-Fa-f:\d.]+)"""
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