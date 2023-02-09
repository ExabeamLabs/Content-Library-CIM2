#### Parser Content
```Java
{
Name = vmware-nsx-str-app-activity-nsxedge
  Vendor = VMware
  Product = VMware NSX
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ NSX """, """ comp="nsx-edge"""", """ level="""", """ subcomp="""" ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """({host}[\w.-]+)\sNSX\s""",
    """\sNSX\s\d+\s(-|({log_source}[^\s]+))""",
    """\slevel="({severity}[^"]+)""",
    """\serrorCode="({error_code}[^"]+)""",
    """\ssubcomp="({category}[^"]+)""",
    """NSX\s\d+\s\S+\s\[[^\]]+\]\s*\[({operation}[^\]]+)\]""",
    """\]\s+(\s+|({additional_info}[^"]+?))\s*"*$""",
  ]


}
```