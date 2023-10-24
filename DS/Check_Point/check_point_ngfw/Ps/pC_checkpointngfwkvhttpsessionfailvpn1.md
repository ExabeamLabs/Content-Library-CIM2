#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-fail-vpn1
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [ """ProductName ="""", """VPN-1 & FireWall-1""" ]
  Fields = [
    """ProductName ="({product_name}VPN-1 & FireWall-1)"""",
    """user="({user}[\w\.\-]{1,40}\$?)"""",
    """\Wxlatesrc="({src_translated_ip}[a-fA-F0-9.:]+)"""",
    """(\d{2}:){2}\d{2}(\+|\-){1,2}\d{1,2}:\d{2}\s+({host}[A-Fa-f0-9.:]+)\s""",
    """({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2})((\+|\-){1,2}\d{1,2}:\d{2})\s+({host}[A-Fa-f0-9.:]+)\s""",
    """\Wsrc="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wdst="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """https_inspection_action="({action}[^"]+)"""",
    """rule_name="({rule}[^"]+)""""
  ]
  DupFields = [ "action->event_name" ]


}
```