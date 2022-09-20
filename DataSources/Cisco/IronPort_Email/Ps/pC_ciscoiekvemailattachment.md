#### Parser Content
```Java
{
Name = cisco-ie-kv-email-attachment
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = IronPort Email
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ MID """, """FileTypes=""", """FileNames=""", """FileSizes=""" ]
  Fields = [
    """FileTypes=({file_type}[^=]+),\s\w+=""",
    """FileNames=({email_attachment}[^=]+\.({file_ext}[^"]+)),\s\w+=""",
    """FileSizes=({bytes}\d+)""",
    """MID ({alert_id}\d+)"""
  ]


}
```