#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-network-session-success-netconn"
  ParserVersion = "v1.0.0"
  Vendor = "VMware"
  Product = "Carbon Black EDR"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """"type":"endpoint.event.netconn""""
    """destinationServiceName ="""
    """"process_username":""""
    """"event_origin":"EDR""""
  ]
  Fields = [
    """\"+process_cmdline\"+:\"+\s*({process_command_line}[^\"]+?)\s*\"+,"""
    """\"+process_username\"+:\"+(({domain}[^\\,]+)\\+)?(Citrix Delivery Services Resources|SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\"+"""
    """\"+process_pid\"+:({process_id}\d+)"""
    """\"+device_name\"+:\s*\"+(\w+\\+)?({host}[^.\"]+)"""
    """\"+sensor_action\"+:\"+({result}[^\"]+)\"+"""
    """\"+process_path\"+:\"+((?i)(SYSTEM)|({process_path}({process_dir}[^\"]+(\\|\/)+)?({process_name}[^\"]+)))\""""
    """\"+action\"+:\"+({action}[^\"]+)?\"*"""
    """\"+parent_cmdline\"+:\"+\s*({parent_process_command_line}[^,\"]+)"""
    """\"+parent_pid\"+:({parent_process_id}\d+)"""
    """\"+process_guid\"+:\"+({process_guid}[^\"]+)?\"*\,"""
    """\"+parent_guid\"+:\"+({parent_process_guid}[^\"]+)?\"*\,"""
    """\"+alert_id\"+:\"+({alert_id}[^,]\"+)?\,"""
    """\"+type\"+:\"+({operation_type}[^\"]+)\"+"""
    """\"device_id\"+:\"+({device_id}[^\",]+)"""
    """\"device_external_ip\"+:\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\"device_timestamp\"+:\"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """\"parent_path\":\"({parent_process_path}({parent_process_dir}[^\"]+(\\|\/)+)?({parent_process_name}[^\"]+))\""""
  ]


}
```