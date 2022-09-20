#### Parser Content
```Java
{
Name = lumension-l-kv-peripheral-storage-insert-usb
Vendor = "Lumension"
Product = "Lumension"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """raw_event_id"""
  """raw_g_hostname"""
]
Fields = [
  """\sraw_g_hostname="+({dest_host}[^"]+)"+,"""
  """\sraw_event_id="+({operation}[^"]+)"+,"""
  """\sraw_ntuser="+(?:({domain}\w+)\\)?({user}[^"]+?)""""
  """\sraw_aduser="+(?=\w)({user_dn}.+?)""""
  """\|devicename=({device_id}[^,\|]+)"""
  """\|devicename=([^,]+),\s+({device_type}[^,;]+),\s+"""
  """\|filesize=({hex_bytes}[^\|]+)"""
  """\|path=+(?=\w)({file_path}.+?)\|"""
  """path=.*\\({file_name}(?:[^\\|]+(?=\.))({file_ext}\.[^\\|]+)?|[^\\|]+)\|\w+="""
  """\|processname=+(?=\w)({process_name}.+?)\|"""
  """\|reason=+(?=\w)({activity_details}.+?)\|"""
]
ParserVersion = "v1.0.0"


}
```