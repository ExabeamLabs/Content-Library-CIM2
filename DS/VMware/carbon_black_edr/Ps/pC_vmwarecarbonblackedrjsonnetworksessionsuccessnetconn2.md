#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-json-network-session-success-netconn-2"
  Vendor = "VMware"
  ParserVersion = "v1.0.0"
  Product = "Carbon Black EDR"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """netconn"""
    """carbonblack"""
    """sensor_action"""
  ]
  Fields = [
    """({time}\d+-\d+-\d+ \d+:\d+:\d+.\d\d\d)"""
    """\"+process_cmdline\"+:\"+({process_command_line}[^\"]+)\"+"""
    """\"+process_username\"+:\"+(NT AUTHORITY\\+|(({domain}[^\\,]+)\\+))?(SYSTEM|({user}[^\",]+))\"+"""
    """\"+process_pid\"+:({process_id}\d+)"""
    """\"+device_name\"+:\s*\"+(\w+\\+)?({host}[^.\"]+)"""
    """\"+sensor_action\"+:\"+({action}[^\"]+)\"+"""
    """\"+process_path\"+:\"+({process_path}({process_dir}[^\"]+(\\|\/)+)?({process_name}[^\"]+))\""""
    """\"+action\"+:\"+({action}[^\"]+)?\"*"""
    """\"+parent_cmdline\"+:\"+({parent_process_command_line}[^,]+\"+)?\"\,"""
    """\"+parent_pid\"+:({parent_process_id}\d+)"""
    """\"+process_guid\"+:\"+({process_guid}[^\"]+)?\"*\,"""
    """\"+parent_guid\"+:\"+({parent_process_guid}[^\"]+)?\"*\,"""
    """\"+alert_id\"+:\"+({alert_id}[^,]\"+)?\,"""
    """\"+type\"+:\"+({operation_type}[^\"]+)\"+"""
    """\"+local_ip\"+:\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\"+remote_ip\"+:\"+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\"+remote_port\"+:({dest_port}\d+)"""
    """\"+local_port\"+:({src_port}\d+)"""
    """netconn_protocol\"+:\"+(PROTO_)?({protocol}[^\"]+)"""
  ]
  DupFields = [
    "operation_type->event_name"
  ]


}
```