#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-endpoint-activity-apicall
  Product = Carbon Black EDR
  Conditions = [ """requestClientApplication=""" , """"type":"endpoint.event.apicall"""", """destinationServiceName =""", """"process_username":"""" ]
  ParserVersion = "v1.0.0"

carbonblack-edr = {
    Vendor = VMware
    Product = Carbon Black EDR
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
    Fields = [
      """"+process_cmdline"+:"+\s*({process_command_line}[^"]+?)\s*"+,""",
      """"+process_username"+:"+(({domain}[^\\,]+)\\+)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[^",]+))"+""",
      """"+process_pid"+:({process_id}\d+)""",
      """"+device_name"+:"+([^\\"]+\\+)?({host}[^"]+)"+""",
      """"+sensor_action"+:"+({action}[^"]+)"+""",
      """"+process_path"+:"+((?i)(SYSTEM)|({process_path}({process_dir}[^"]+(\\|\/)+)?({process_name}[^"]+)))"""",
      """"+action"+:"+({action}[^"]+)?"*""",
      """"+parent_cmdline"+:"+\s*({parent_process_command_line}[^"]+?)\s*",""",
      """"+parent_pid"+:({parent_process_id}\d+)""",
      """"+process_guid"+:"+({process_guid}[^"]+)?"*\,""",
      """"+parent_guid"+:"+({parent_process_guid}[^"]+)?"*\,""",
      """"+alert_id"+:"+({alert_id}[^,]"+)?\,""",
      """"+type"+:"+({operation_type}[^"]+)"+""",
      """"device_id"+:"+({device_id}[^",]+)""",
      """"device_external_ip"+:"+({dest_ip}[^",]+)""",
      """"device_os"+:"+({os}[^",]+)""",
      """"device_timestamp"+:"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
      """"parent_path":"({parent_process}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""",
    
}
```