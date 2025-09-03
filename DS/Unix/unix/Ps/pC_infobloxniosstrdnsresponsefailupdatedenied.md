#### Parser Content
```Java
{
Name = infoblox-nios-str-dns-response-fail-updatedenied
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss" ]
  Conditions = [ """ named[""", """ update """, """ denied""" ]
  Fields = [
    """\d\d:\d\d:\d\d(\.\d+Z?)? (::ffff:)?({host}[\w\.-]+)""",
    """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)""",
    """\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(#({src_port}\d+))"""
    """({action}denied)"""
    """named\[\S+?:\s+({additional_info}[^~]+?)\s*$"""
  ]


}
```