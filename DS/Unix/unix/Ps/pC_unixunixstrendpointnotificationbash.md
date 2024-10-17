#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-bash
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ bash[""" , """]: """ ]
  Fields = [
    """({time}\w+\s*\d+ \d\d:\d\d:\d\d)\s*({host}[^\s]+)\s*bash\[""",
    """bash\[({process_id}\d+)\]:\s*({additional_info}.+?)\s*$""",
  ]


}
```