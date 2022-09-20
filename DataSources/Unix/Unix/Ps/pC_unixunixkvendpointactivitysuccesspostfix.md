#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-activity-success-postfix
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ EVENT=""", """ DETAILS=""", """postfix""" ]
  Fields = [
    """({event_category}\w+)\s*EVENT=({event_name}.+?)\s*\w+=""",
    """\sOBJECT=({object}.+?)\s*\w+=""",
    """\sUSER=({user}.+?)\s*\w+=""",
# origin is removed
    """time=({start_time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """endtime=({end_time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d)""",
# process_users is removed
    """TYPE=({category}.+?)\s*\w+="""
  ]
  DupFields = [ "start_time->time" ]


}
```