#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-leef-alert-trigger-success-watchlist"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch_sec"
Conditions = [
  """0|CB|CB|"""
  """watchlist.hit"""
]
Fields = [
  """timestamp=({time}\d{10})"""
  """hostname=({host}[^=]+?)\s+\w+="""
  """0\|CB\|CB\|[^|]+\|({alert_type}[^|]+)\|"""
  """computer_name=({dest_host}[^=]+?)\s+\w+="""
  """interface_ip=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """username=(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
  """sensor_id=({sensor_id}[^=]+?)\s+\w+="""
  """\W(process_)?md5=(|({hash_md5}[^=]+?))(\s+\w+=|\s*$)"""
  """cmdline=\"+(\\+\?+\\+)?({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\"+"""
  """alert_severity=({alert_severity}[^=]+?)\s+\w+="""
  """alert_type=({alert_type}[^=]+?)\s+\w+="""
  """watchlist_name=({additional_info}[^=]+?)(\s+\w+=|\s*$)"""
  """unique_id=\{?({alert_id}[^=]+?)\}?\s+\w+="""
  """os_type=({os}[^=]+?)\s+\w+="""
  """process_name=({process_name}[^=]+?)\s+\w+="""
  """\s(process_)?path=({path}[^=]+?)\s+\w+="""
  """\s(process_)?path=({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+?))\s*(\w+=|")"""
  """process_guid=({process_guid}[^=]+?)\s+\w+="""
  """ioc_value=({ioc}[^=]+?)\s+\w+="""
  """ioc_attr=({ioc}[^=]+?)\s+\w+="""
  """ioc_query_string=\(({ioc}[^=]+?)\)"""
  """parent_guid=({parent_process_guid}[^=]+?)\s*(\w+=|$)"""
  """parent_name=({parent_process_name}[^=]+?)\s*(\w+=|$)"""
  """cmdline=({process_command_line}[^=]+?)\s*(\w+=|$)"""
  """host_type=(|({host_type}[^=]+?))\s*(\w+=|$)"""
  """\W+type=({alert_name}[^=]+?)\s+\w+="""
]
SOAR {
  IncidentType = "generic"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->description"
    "alert_severity->sourceSeverity"
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
        "dest_ip->ip_address"
        "dest_host->host_name"
      ]
    

}
```