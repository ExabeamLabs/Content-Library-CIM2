#### Parser Content
```Java
{
Name = hp-arubaos-str-endpoint-login-success-03362
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ 03362 """, """ auth:""" ]

aruba-switch-info = {
  Vendor = HP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s({event_code}\S+)\s({event_name}[^\s:]+):\s*({additional_info}[^\n"]+?)\s*$""",
    """port\s({dest_port}\d+)""",
    """User '({user}[^'\s]+)""",
    """from ({src_ip}[A-Fa-f\d:.]+)"""
  
}
```