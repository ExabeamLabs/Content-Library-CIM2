#### Parser Content
```Java
{
Name = hp-arubacpm-kv-app-notification-success-cppmsystemstat
  ParserVersion = v1.0.0
  Product = Aruba ClearPass Policy Manager
  Conditions = [ """ CPPM_System_Stat """, """swap_size_used=""", """slash_size_used=""" ]
  Fields = ${DLArubaParsersTemplates.aruba-clearpass-info.Fields}[
# swap_size_used is removed
# slash_size_used is removed
# swap_memory_avail is removed
# system_memory_avail is removed
# cpu_raw_user is removed
# cpu_raw_nice is removed
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