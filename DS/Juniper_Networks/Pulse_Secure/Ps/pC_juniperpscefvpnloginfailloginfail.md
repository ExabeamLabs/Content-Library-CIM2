#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-fail-loginfail
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Pulse""", """|Login failed""", """Reason:""" ]
  Fields = [
   """\srt=({time}\d+)""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\ssuser=(System|({user}.+?))\s+sproc=""",
    """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """Reason:\s+({failure_reason}.+?)(\|[^\s]*)?\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```