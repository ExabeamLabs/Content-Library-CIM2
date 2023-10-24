#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-notification-sshdset
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """sshd[""", """ Set """ ]
  Fields = [
    """({host}\S+) sshd\[""",
    """\ssshd\[\d+\]:\s*({additional_info}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```