#### Parser Content
```Java
{
Name = unix-unix-str-app-activity-gofer
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ goferd: [""", """][""", """ gofer.""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({dest_ip}[^\s]+)\s*({host}[^\s]+)\s*goferd:""",
    """({result}failed)""",
    """({additional_info}failed.+?)\s*$""",
  ]
  ParserVersion = "v1.0.0"


}
```