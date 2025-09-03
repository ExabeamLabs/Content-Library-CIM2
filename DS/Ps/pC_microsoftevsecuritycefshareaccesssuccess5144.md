#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-share-access-success-5144"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """A network share object was deleted"""
  """Microsoft-Windows-Security-Auditing:5144|"""
]
ParserVersion = "v1.0.0"

windows-events-3.Fields} [
      """\Wdhost=\s*({dest_host}[\w\-.]+?)(\s+(\w+|\w+\.\w+)=|\s*$)""",
      """\sahost=({host}[^\s]+)""",
      """({event_name}A member was removed from a security-enabled universal group)""",
      """({event_code}4757)""",
	  """suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
	  """duser=({dest_user}[^=]+)\s\w+=""",
	  """sntdom=({domain}[^=\\\s]+)""",
	  """dntdom=({dest_domain}[^=\\\s]+)""",
	  """cs6=(({group_domain}[^\\=]+)\\+)?({group_name}[^=]+?)\s\w+="""
   
}
```