#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-fail-loginfail
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Pulse""", """|Login failed""", """Reason:""" ]
  Fields = [
   """\srt=({time}\d{13})""",
    """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sdvchost=({host}[^\s]+)""",
    """\ssuser=(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+sproc=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Reason:\s+({failure_reason}.+?)(\|[^\s]*)?\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```