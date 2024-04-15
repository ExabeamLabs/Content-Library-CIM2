#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-mix-file-filemod"
  ParserVersion = "v1.0.0"
  Conditions = [ """filemod""" , """carbonblack""" , """sensor_action""" ]

carbonblack-endpoint = { 
    Vendor = VMware
    Product = Carbon Black EDR
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Fields = [
    """({time}\d+-\d+-\d+ \d+:\d+:\d+.\d\d\d)""",
    """"+process_cmdline"+:"+({process_command_line}[^"]+)"+""",
    """"+process_username"+:"+(({domain}[^\\,]+)\\+)?(SYSTEM|({user}[^",]+))"+""",
    """"+process_pid"+:({process_id}\d+)""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+sensor_action"+:"+({action}[^"]+)"+""",
    """"+process_path"+:"+({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))"""",
    """"+action"+:"+({action}[^"]+)?"*""",
    """"+parent_cmdline"+:"+({parent_process_command_line}[^,]+"+)?"\,""",
    """"+parent_pid"+:({parent_process_id}\d+)""",
    """"+process_guid"+:"+({process_guid}[^"]+)?"*\,""",
    """"+parent_guid"+:"+({parent_process_guid}[^"]+)?"*\,""",
    """"+alert_id"+:"+({alert_id}[^,]"+)?\,""",
    """"+type"+:"+({operation_type}[^"]+)"+"""

   
}
```