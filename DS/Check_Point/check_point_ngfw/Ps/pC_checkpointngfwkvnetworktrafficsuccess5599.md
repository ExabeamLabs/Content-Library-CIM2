#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-success-5599
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """; product:""""
  """ CheckPoint 5599 """
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) ({host}[\w.\-]+) CheckPoint"""
  """product:"({product_name}[^"]+)""""
  """received_bytes:"({bytes_in}\d+)""""
  """sent_bytes:"({bytes_out}\d+)""""
  """origin:"({origin_ip}[^"]+)""""
  """originsicname:"({origin_sic_name}[^"]+)""""
  """loguid:"({log_uid}[^"]+)""""
  """policy_name=({policy_name}.+?)[\\\]]"""
  """proto:"({protocol}[^"]+)""""
  """src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """s_port:"({src_port}\d+)""""
  """message_info:"({additional_info}[^"]+)""""
  """dst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """ifname:"({src_interface}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```