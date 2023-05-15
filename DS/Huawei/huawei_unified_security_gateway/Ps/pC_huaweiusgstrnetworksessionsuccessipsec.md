#### Parser Content
```Java
{
Name = huawei-usg-str-network-session-success-ipsec
  Vendor = Huawei
  Product = Huawei Unified Security Gateway
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """IPSEC/""", """/STREAM""", """srcip_begin=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d),\S+\s+({host}[\w\.\-]+)""",
    """\Wprotocol=({protocol}.+?)(\s+\w+=|\s*$)""",
    """\Wlocal_ip=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wremote_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s+\w+=|\s*$)""",
    """\Wsend_bytes=({bytes_out}\d+)""",
    """\Wrecv_bytes=({bytes_in}\d+)""",
  ]


}
```