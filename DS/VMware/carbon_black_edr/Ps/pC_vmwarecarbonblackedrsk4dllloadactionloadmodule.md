#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-dll-load-actionloadmodule
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """endpoint.event.moduleload""", """"process_username":"""", """"event_origin":"EDR"""", """"modload_name":"""", """"action":"ACTION_LOAD_MODULE"""" ]
  Fields = [
    """"+process_cmdline"+:"+\s*({process_command_line}.+?)\s*"+""",
    """"+process_username"+:"+(({domain}[^\\,]+)\\+)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"+""",
    """"+process_pid"+:({process_id}\d+)""",
    """"+device_name"+:"+({host}[^"]+)"+""",
    """"+sensor_action"+:"+({action}[^"]+)"+""",
    """"+process_path"+:"+({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+))"""",
    """"+action"+:"+({action}[^"]+)?"*""",
    """"+parent_cmdline"+:"+\s*({parent_process_command_line}[^,"]+)""",
    """"+parent_pid"+:({parent_process_id}\d+)""",
    """"+process_guid"+:"+({process_guid}[^"]+)?"*\,""",
    """"+parent_guid"+:"+({parent_process_guid}[^"]+)?"*\,""",
    """"+alert_id"+:"+({alert_id}[^,]"+)?\,""",
    """"+type"+:"+({operation_type}[^"]+)"+""",
    """"device_id"+:"+({device_id}[^",]+)""",
    """"device_external_ip"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"device_timestamp"+:"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  ]


}
```