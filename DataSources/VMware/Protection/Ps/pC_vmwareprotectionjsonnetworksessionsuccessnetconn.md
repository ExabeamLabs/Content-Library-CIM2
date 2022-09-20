#### Parser Content
```Java
{
Name = vmware-protection-json-network-session-success-netconn
  Vendor = VMware
  Product = Protection
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
    """local_ip\":\"({src_ip}[^\"]+)""",
    """remote_ip\":\"({dest_ip}[^\"]+)\"""",
    """remote_port\":({dest_port}\d+)""",
    """domain\":\"({web_domain}[^\"]+)"""
] 


}
```