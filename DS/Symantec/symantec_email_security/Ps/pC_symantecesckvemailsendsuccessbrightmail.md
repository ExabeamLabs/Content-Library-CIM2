#### Parser Content
```Java
{
Name = symantec-esc-kv-email-send-success-brightmail
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [ """[Brightmail]""", """ A message from """, """ returned Disposition:""" ]
    Fields = [
      """\s({host}[\w\.-]+)\s+bmserver""",
      """A message from\s+<({src_email_address}[^\s@]+@[^\s@>]+)>?\s+source""",
      """source\s+<?({direction}\w+)+>?\s+to""",
      """to\s+<?({email_recipients}[^<>]+)>?\s+using""",
      """to\s+<?({dest_email_address}[^\s@<]+@[^\s@>]+)>?\s+using""",
    ]
	ParserVersion = "v1.0.0"
  

}
```