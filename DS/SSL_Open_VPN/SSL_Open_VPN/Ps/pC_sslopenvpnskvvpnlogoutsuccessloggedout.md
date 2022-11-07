#### Parser Content
```Java
{
Name = sslopenvpn-s-kv-vpn-logout-success-loggedout
  Conditions = [ """id=ArrayOS""", """logged out successfully""", """type=vpn""" ]
  ParserVersion = "v1.0.0"

openvpn-events = {
  Vendor = SSL Open VPN
  Product = SSL Open VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\Wtime="({time}\d\d\d\d-\d+-\d+ \d\d:\d\d:\d\d)""",
    """\Wuser=({user}[^\s]+)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst=(0\.0\.0\.0|({dest_ip}[A-Fa-f:\d.]+))""",
    """\Wsport=({src_port}\d+)""",
    """\Wdport=({dest_port}\d+)""",
    """\Wdstname=({src_host}[\w\-.]+)""",
    """\Wgroup info:\s*\(({group_info}[^\)]+)""",
    """\Wlogin method:?\s*\(({login_method}[^\)]+)""",
    """\Wreason\s*\(({failure_reason}[^\)]+)""",
    """\Wsession id\s+({session_id}[^,]+)""",
    """\Wduration\s+({duration}[^.]+)""",
    """\WTCP tunnel\(({src_translated_ip}[A-Fa-f:\d.]+)\)""",
    """\Wclientip\(({src_translated_ip}[A-Fa-f:\d.]+)\)""",
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"

}
```