#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-leef-alert-trigger-success-feed"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch_sec"
Conditions = [
  """0|CB|CB|"""
  """type=feed."""
]
Fields = [
  """\Wtimestamp=({time}\d{10})"""
  """\d+:\d+:\d+Z\s+({host}[\w\-\.]+)\s+[^\[\]]*\[\d+\]:"""
  """hostname=({host}[^=]+?)\s+\w+="""
  """0\|CB\|CB\|[^|]*\|({alert_type}[^|]+)\|"""
  """\Wcomputer_name=(|({dest_host}[^=]+?))(\s+\w+=|\s*$)"""
  """\Winterface_ip=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """\Wusername=(({domain}[^\\]+)\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """\Wsensor_id=(|({sensor_id}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wioc_type=md5[^@]+?ioc_value=(|({hash_md5}[^=]+?))(\s+\w+=|\s*$)"""
  """\W(process_)?md5=(|({hash_md5}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wcmdline=\"+(\\+\?+\\+)?({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\"+"""
  """\Wunique_id=(|({alert_id}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wos_type=(|({os}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wprocess_name=(|({process_name}[^=]+?))(\s+\w+=|\s*$)"""
  """\W(process_)?path=(|({path}[^=]+?))(\s+\w+=|\s*$)"""
  """\W(process_)?path=(|({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+?)))(\s+\w+=|\s*$)"""
  """\Wprocess_guid=(|({process_guid}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wioc_value=(|({ioc}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wioc_query_string=(|({ioc}[^=]+?))(\s+\w+=|\s*$)"""
  """\Wparent_guid=(|({parent_process_guid}[^=]+?))\s*(\w+=|$)"""
  """\Wparent_name=(|({parent_process_name}[^=]+?))\s*(\w+=|$)"""
  """\Wcmdline=\s*({process_command_line}[^=]+?)\s*(\w+=|$)"""
  """\Wtype=(|({alert_type}[^\"]+?))(\s+\w+=|\s*$)"""
  """\Wreport_score=({alert_severity}\d+)"""
  """\Whost_type=(|({host_type}[^\"]+?))(\s+\w+=|\s*$)"""
  """feed_name=(|({alert_name}[^\"]+?))(\s+\w+=|\s*$)"""
]
DupFields = [
  "ioc->additional_info"
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