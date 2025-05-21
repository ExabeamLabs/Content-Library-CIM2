#### Parser Content
```Java
{
Name = hp-arubaos-str-endpoint-logout-success-03363
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ 03363 """, """ auth:""" ]

aruba-switch-info = {
  Vendor = HP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)\s({event_code}\S+)\s({event_name}[^\s:]+):\s*({additional_info}[^\n"]+?)\s*$""",
    """port\s({dest_port}\d+)""",
    """User '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'""",
    """from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  
}
```