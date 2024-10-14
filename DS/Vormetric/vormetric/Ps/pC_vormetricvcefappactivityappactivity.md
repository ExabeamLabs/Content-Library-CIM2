#### Parser Content
```Java
{
Name = vormetric-v-cef-app-activity-appactivity
  Vendor = Vormetric
  Product = Vormetric
  TimeFormat = "epoch"
  Conditions = [
    """CEF:""",
    """|Vormetric, Inc.|"""
  ]
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wdvchost=({host}[\w\-.]+)""",
    """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\Wshost=({src_host}[^\s]+)""",
# logger is removed
# spid is removed
    """\Wrequest=({request}.+?)\s+(\w+=|$)""",
# vds_otype is removed
# vds_oname is removed
    """\Wold_value=\[({old_value}[^\]]+)""",
    """\Wnew_value=\[({new_value}[^\]]+)""",
    """CEF:([^\|]*\|){1}({app}[^\|]+)""",
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```