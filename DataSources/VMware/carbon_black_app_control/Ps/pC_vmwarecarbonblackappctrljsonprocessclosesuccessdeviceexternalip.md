#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-json-process-close-success-deviceexternalip
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = carbon black app control
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """endpoint.event.procend""", """process_cmdline""", """device_external_ip""" ]
  Fields = [
    """({time}\d+-\d+-\d+ \d+:\d+:\d+.\d+)\sGMT""",
    """"+process_cmdline"+:"+\s*({process_command_line}[^"]+?)\s*"+""",
    """"+device_external_ip"+:"+({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"+""",
    """"+process_pid"+:({process_id}\d+)""",
    """"+device_name"+:"+({host}[^"]+)"+""",
# sensor_action is removed
    """"+process_path"+:"+({process_path}({process_dir}(:?[\w:]+)?[^"]*\\)({process_name}[^"]+))""",
    """"+action"+:"+({action}[^"]+)"+""",
    """"+parent_cmdline"+:"+\s*({parent_process_command_line}[^,"]+)""",
    """"+parent_pid"+:({parent_process_id}\d+)""",
    """"+process_guid"+:"+({process_guid}[^,"]+)?"*\,""",
    """"+parent_guid"+:"+({parent_process_guid}[^,"]+)?"*\,""",
    """"+alert_id"+:"+({alert_id}[^,"]"+)?\,""",
    """"+type"+:"+({event_category}[^"]+)"+""",
    """"device_id"+:"+({device_id}[^",]+)""",
    """"+device_os"+:"+({os}[^"]+)"+"""
    """"device_timestamp"+:"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"+process_username"+:"+(({domain}[^\\,]+)\\+)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^"]+))"+""",
  ]
  DupFields = ["event_category->operation_type"]


}
```