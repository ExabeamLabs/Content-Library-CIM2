#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-success-named
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """named[""", """]: xfer-in: transfer of '""" ]
  Fields = [
    """\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d(\.\S+)?\s({host}\S+)\snamed""",
    """({operation}transfer)""",
    """transfer of '({zone}[^']+?)(\/[^']+)?'""",
    """transfer of '[^']+'\sfrom\s({host_record}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """({additional_info}transfer of[^=]+?)\s*$""",
    """Transfer status:\s({action}[^\s]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```