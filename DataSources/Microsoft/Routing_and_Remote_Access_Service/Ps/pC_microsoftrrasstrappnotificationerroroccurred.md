#### Parser Content
```Java
{
Name = microsoft-rras-str-app-notification-erroroccurred
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Routing and Remote Access Service
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """CoId= {""", """The following error occurred""" ]
  Fields = [
    """CoId=\{({session_id}[^\{\}]+?)\}""",
    """\WUserName:\s*(<|&lt;)({user}[^<>]+?)(>|&gt;)""",
    """\WSpecifically,\s*({failure_reason}[^\.]+)""",
  ]


}
```