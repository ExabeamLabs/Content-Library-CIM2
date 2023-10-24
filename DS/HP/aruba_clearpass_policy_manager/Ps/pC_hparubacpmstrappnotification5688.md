#### Parser Content
```Java
{
Name = hp-arubacpm-str-app-notification-5688
  ParserVersion = v1.0.0
  Product = Aruba ClearPass Policy Manager
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy","MMM dd HH:mm:ss yyyy"]
  Conditions = [ """awc[5688]:""", """wsc:""" ]
  Fields = ${DLArubaParsersTemplates.aruba-clearpass-info.Fields}[
    """awc\[5688\]:\s*({additional_info}[^"\$]+?)\s*("|$)""",
    """({event_code}awc\[5688\])"""
  ]

aruba-clearpass-info = {
  Vendor = HP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\d+:\d+:\d+ ({host}[\w\-\.]+)\s*({time}\d+-\d+-\d+\s*\d+:\d+:\d+)""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d+)\s*\d{1,3}\.\d{1,3}.\d{1,3}.\d{1,3}\s*\s*({host}[\w\.:\-]+)\s*<""",
    """({event_name}CPPM_[^\s]+)""",
    """mac_address=({src_mac}[^,]+)""",
    """ip_address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  
}
```