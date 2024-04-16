#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624-4"
Conditions = [
""""event-id":4624"""
""""message":"An account was successfully logged on"""
""""user":"""
]
ParserVersion = "v1.0.0"

windows-events-3.Fields} [
      """({event_name}A member was removed from a security-enabled universal group)""",
      """({event_code}4757)""",
	  """suser=({user}[\w\.\-]{1,40}\$?)\s\w+=""",
	  """duser=({dest_user}[^=]+)\s\w+=""",
	  """sntdom=({domain}[^=\\\s]+)""",
	  """dntdom=({dest_domain}[^=\\\s]+)""",
	  """cs6=(({group_domain}[^\\=]+)\\+)?({group_name}[^=]+?)\s\w+="""
   
}
```