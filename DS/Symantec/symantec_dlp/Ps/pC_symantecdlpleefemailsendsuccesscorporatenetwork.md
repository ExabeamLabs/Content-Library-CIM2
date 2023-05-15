#### Parser Content
```Java
{
Name = symantec-dlp-leef-email-send-success-corporatenetwork
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """LEEF:""", """|Symantec|DLP|""", """SMTP""", """Off the Corporate Network""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[\+\-]\d+:\d+\s""",
    """\s({host}[\w\-.]+)\s+LEEF:""",
    """LEEF:([^\|]*\|){4}(N\/A)*\s*({last_name}[^\\\/,\_\s]+?),\s*({first_name}[^\\\/,\_]+?)\s+\w+\s+({file_name}[^\s]+)""",
    """\d+:\d+:\d+\s+(AM|PM|am|pm)\s*SMTP\s*({email_recipients}({dest_email_address}[^\\\/\s@,;"]+@[^\\\/\s@,;"]+)[^\s]*?)November""",
    """\d+:\d+:\d+\s+(AM|PM|am|pm)\s*N\/A\s*({src_email_address}[^\\\/\s@,;"]+@[^\\\/\s@,;"]+?)\s*({dest_host}\w\w\-\w+\d\d+)\s*(|({email_subject}.*?))\s*(N\/A)+""",
    """\|N\/AN\/A((N\/A)|(null)|({file_name}(?!null|N\/A).+?))\snull"""
  ]
  DupFields = [ "dest_email_address->external_address" ]
  ParserVersion = "v1.0.0"


}
```