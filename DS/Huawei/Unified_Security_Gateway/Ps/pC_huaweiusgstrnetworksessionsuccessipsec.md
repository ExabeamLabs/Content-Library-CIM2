#### Parser Content
```Java
{
Name = huawei-usg-str-network-session-success-ipsec
  Vendor = Huawei
  Product = Unified Security Gateway
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """IPSEC/""", """/STREAM""", """srcip_begin=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
    """\Wprotocol=({protocol}.+?)(\s+\w+=|\s*$)""",
    """\Wlocal_ip=({src_ip}[a-fA-F\d.:]+)""",
    """\Wremote_ip=({dest_ip}[a-fA-F\d.:]+)(\s+\w+=|\s*$)""",
    """\Wsend_bytes=({bytes_out}\d+)""",
    """\Wrecv_bytes=({bytes_in}\d+)""",
  ]


}
```