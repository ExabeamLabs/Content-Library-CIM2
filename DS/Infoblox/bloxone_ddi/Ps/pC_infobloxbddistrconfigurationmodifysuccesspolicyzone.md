#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-success-policyzone
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """named[""", """]: rpz: (re)loaded policy zone '"""]
  Fields = [
    """\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d(\.\S+)?\s({host}\S+)\snamed""",
    """({operation}\(re\)loaded policy zone)""",
    """\(re\)({event_name}loaded policy zone) '({zone}[^']+)""",
    """({additional_info}\(re\)loaded policy zone[^=]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```