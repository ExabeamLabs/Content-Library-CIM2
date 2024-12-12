#### Parser Content
```Java
{
Name = infoblox-bddi-str-configuration-modify-success-transfersuccess
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """named[""", """ Transfer status: """, """ transfer of """ ]
  Fields = [
    """\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d(\.\S+)?\s({host}\S+)\snamed""",
    """({operation}transfer)""",
    """transfer of '({zone}[^']+?)(\/[^']+)?'""",
    """({additional_info}transfer of[^=]+?)\s*$""",
    """Transfer status:\s({action}[^\s]+?)\s*$"""
  ]
  DupFields = [
  "action->result"
  ]
  ParserVersion = "v1.0.0"


}
```