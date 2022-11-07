#### Parser Content
```Java
{
Name = vmware-carbonblackceedr-sk4-network-session-success-edr
  Vendor = VMware
  Product = Carbon Black Cloud Enterprise EDR
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event_origin":"EDR"""", """"type":"endpoint.event.netconn_proxy"""", """"process_path":""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"+process_username"+:\s*"+(({email_address}[^@,"]+@[^",]+)|(({domain}[^\\"]+?)\\+)?({user}[^"]+))"+""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+reason"+:\s*"+({additional_info}[^"]+?)"+""",
    """"+device_os"+:\s*"+({os}[^"]+?)"+""",
    """"+state"+:\s*"+({state}[^"]+?)"+""",
    """"+type"+:\s*"+({event_name}[^"]+?)"+""",
    """"+process_pid"+:\s*({process_id}\d+)""",
    """"+process_path"+:"+({process_path}({process_dir}[^"]+)\\({process_name}[^"]+))"""",
    """"+parent_path"+:"+({parent_process}({parent_process_dir}[^"]+)\\({parent_process_name}[^"]+))"""",
    """"+local_ip"+:"+({src_ip}[A-Fa-f.:\d]+)"+""",
    """"+local_port"+:({src_port}\d+)""",
    """"+action"+:"+({result}[^"]+)"+""",
    """"+process_cmdline"+:"+\s*({process_cmd}[^"]+?)\s*"+""",
    """"+parent_cmdline"+:"+\s*({parent_cmd}[^,"]+)""",
    """"+process_guid"+:"+({process_guid}[^"]+)""",
    """"+parent_guid"+:"+({parent_process_guid}[^"]+)""",
  ]
  DupFields = ["event_name->operation_type"]
ParserVersion = "v1.0.0"


}
```