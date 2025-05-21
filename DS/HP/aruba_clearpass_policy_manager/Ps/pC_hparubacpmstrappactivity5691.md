#### Parser Content
```Java
{
Name = hp-arubacpm-str-app-activity-5691
  ParserVersion = v1.0.0
  Product = Aruba ClearPass Policy Manager
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy","MMM dd HH:mm:ss yyyy"]
  Conditions = [ """cli[5691]:""", """wsc:""" ]
  Fields = ${DLHPEParsersTemplates.aruba-clearpass-info.Fields}[
    """({event_code}cli\[5691\])""",
    """cli\[5691\]:\s*({additional_info}[^"\$]+?)\s*("|$)"""
  ]

aruba-clearpass-info = {
  Vendor = HP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d+:\d+:\d+ ({host}[\w\-\.]+)\s*({time}\d+-\d+-\d+\s*\d+:\d+:\d+)""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d+)\s*\d{1,3}\.\d{1,3}.\d{1,3}.\d{1,3}\s*\s*({host}[\w\.:\-]+)\s*<""",
    """({event_name}CPPM_[^\s]+)""",
    """mac_address=({src_mac}[^,]+)""",
    """ip_address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  
}
```