#### Parser Content
```Java
{
Name = hp-arubaos-str-log-enable-04331
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ 04331 """, """ mgr:""" ]

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