#### Parser Content
```Java
{
Name = pan-prisma-kv-app-activity-success-twistlock
  Vendor = Palo Alto Networks
  Product = Prisma Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """Twistlock-Console""", """log_type=""""]
  Fields = [
    """time="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{3,9}Z)""",
    """type="({event_name}[^"]+)"""",
    """log_type="({event_category}[^"]+)"""",
    """image_id="({image_id}[^"]+)"""",
    """image_name="({image_name}[^"]+)"""",
    """vulnerabilities="({vulnerabilities}[^"]+)"""",
    """compliance="({compliance}[^"]+)""",
    """clusters="({clusters}[^"]+)"""
  ]


}
```