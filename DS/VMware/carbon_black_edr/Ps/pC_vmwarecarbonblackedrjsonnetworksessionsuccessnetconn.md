#### Parser Content
```Java
{
Name = vmware-carbonblackedr-json-network-session-success-netconn
  Vendor = VMware
  Product = Carbon Black EDR
  ParserVersion = v1.0.0
  TimeFormat = epoch_sec
  Conditions = [ """"process_guid"""", """ingress.event.netconn""" ]
  Fields = [
    """timestamp\":({time}\d{10})""",
    """\"type\":\"({operation_type}[^\"]+)""",
    """computer_name\":\"({src_host}[^\"]+)""",
    """sensor_id\":({sensor_id}\d+)""",
    """md5\":\"({hash_md5}[^\"]+)""",
    """\"pid\":({process_id}\d+)""",
    """\"process_guid\":\"({process_guid}[^\"]+)""",
    """local_ip\":\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """remote_ip\":\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\"""",
    """remote_port\":({dest_port}\d+)""",
    """domain\":\"({web_domain}[^\"]+)"""
] 


}
```