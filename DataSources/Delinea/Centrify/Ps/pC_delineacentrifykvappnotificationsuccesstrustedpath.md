#### Parser Content
```Java
{
Name = delinea-centrify-kv-app-notification-success-trustedpath
  Vendor = Delinea
  Product = Centrify
  ParserVersion = v1.0.0
  TimeFormat = "epoch"
  Conditions = ["""Centrify Suite|Trusted Path""" , """|Trusted path"""]
  Fields = [
    """utc=({time}\d+)""",
    """user=({user}[^\(\)\s\$]+)"""
    """\d+\|\d+\|({event_name}.+?)\|\d""",
    """status=({action}.+?)\s\w+=""",
    """pid=({process_id}\d+)""",
    """server=(.+?\/)?({src_host}[^.\s]+)"""
   ]


}
```