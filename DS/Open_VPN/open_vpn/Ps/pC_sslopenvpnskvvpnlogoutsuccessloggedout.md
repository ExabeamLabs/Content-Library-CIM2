#### Parser Content
```Java
{
Name = sslopenvpn-s-kv-vpn-logout-success-loggedout
  Conditions = [ """id=ArrayOS""", """logged out successfully""", """type=vpn""" ]
  ParserVersion = "v1.0.0"

openvpn-events = {
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\Wtime="({time}\d\d\d\d-\d+-\d+ \d\d:\d\d:\d\d)""",
    """\Wuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wsport=({src_port}\d+)""",
    """\Wdport=({dest_port}\d+)""",
    """\Wdstname=({dest_host}[\w\-.]+)""",
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