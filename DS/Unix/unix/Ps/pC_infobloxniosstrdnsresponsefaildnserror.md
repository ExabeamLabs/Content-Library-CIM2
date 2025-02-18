#### Parser Content
```Java
{
Name = infoblox-nios-str-dns-response-fail-dnserror
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "MMM dd HH:mm:ss" ]
  Conditions = [ """ named[""", """DNS format error""" ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)""",
    """\d\d:\d\d:\d\d(\.\d+Z?)? (::ffff:)?({host}[\w\-\.]+)""",
    """from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({src_port}\d+))?""",
    """for client\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#?({dest_port}\d+))?"""
    """named\[\S+?:\s+({additional_info}[^"]+)"""
  ]


}
```