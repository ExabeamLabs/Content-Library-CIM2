#### Parser Content
```Java
{
Name = unix-unix-cef-user-switch-success-runuser
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch"
Conditions = [
  """|Unix|Unix|"""
  """|session opened|"""
  """cs1=runuser"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvchost=({host}.+?)\s+(\w+=|$)"""
  """\Wsuid=({user_uid}.+?)\s+(\w+=|$)"""
  """\Wduser=({dest_user}.+?)\s+(\w+=|$)"""
  """\Wcs1=({process_name}.+?)\s+(\w+=|$)"""
  """\Wdhost=({dest_host}.+?)\s+(\w+=|$)"""
]
DupFields = [
  "process_name->event_code"
]
ParserVersion = "v1.0.0"


}
```