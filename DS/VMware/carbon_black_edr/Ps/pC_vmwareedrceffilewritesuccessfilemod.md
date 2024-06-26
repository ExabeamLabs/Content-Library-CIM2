#### Parser Content
```Java
{
Name = "vmware-edr-cef-file-write-success-filemod"
   ParserVersion = v1.0.0
   Conditions = [ """"type":"endpoint.event.filemod"""", """destinationServiceName =""", """"process_username":"""", """"event_origin":"EDR"""" ]
   Fields = ${CarbonBlackParsersTemplates.carbonblack-edr.Fields}[
    """parent_path":"({parent_process}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
   ]

carbonblack-edr {
   Vendor = VMware
   Product = Carbon Black EDR
   TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Fields = [
    """"+process_cmdline"+:"+\s*({process_command_line}[^"]+?)\s*"+,""",
    """"+process_username"+:"+((NT AUTHORITY|({domain}[^\\,]+))\\\\)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^",]+))"+""",
    """"+process_pid"+:({process_id}\d+)""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+sensor_action"+:"+({action}[^"]+)"+""",
    """"+process_path"+:"+((?i)(SYSTEM)|({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+)))"""",
    """"+action"+:"+({action}[^"]+)?"*""",
    """"+parent_cmdline"+:"+\s*({parent_process_command_line}[^,"]+)""",
    """"+parent_pid"+:({parent_process_id}\d+)""",
    """"+process_guid"+:"+({process_guid}[^"]+)?"*\,""",
    """"+parent_guid"+:"+({parent_process_guid}[^"]+)?"*\,""",
    """"+alert_id"+:"+({alert_id}[^,]"+)?\,""",
    """"+type"+:"+({operation_type}[^"]+)"+""",
    """"device_id"+:"+({device_id}[^",]+)""",
    """"device_external_ip"+:"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"device_timestamp"+:"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """"+device_os"+:"+({os}[^"]+)"+"""
  
}
```