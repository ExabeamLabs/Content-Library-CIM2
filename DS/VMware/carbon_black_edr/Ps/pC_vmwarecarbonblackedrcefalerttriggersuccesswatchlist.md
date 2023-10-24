#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-cef-alert-trigger-success-watchlist"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch_sec"
Conditions = [
"""watchlist.hit"""
"""watchlist_name"""
]
Fields = [
""""hostname"\s*:\s*"({host}[^\s"]+)""""
""""type":"({alert_type}[^"]+)"""
""""timestamp"\s*:\s*({time}\d{10})"""
"""computer_name":"({dest_host}[^"]+)"""
"""interface_ip"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""username"+:"+(({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""
"""sensor_id":"?({sensor_id}[^"\,]+)"""
"""md5":"({hash_md5}[^"]+)"""
"""alert_severity"+:"+({alert_severity}[^"]+)"""
"""watchlist_name"+:"+({alert_name}[^"]+)"""
"""unique_id"+:"+\{?({alert_id}[^\}"]+)"""
"""os_type"+:"+({os}[^"]+)"""
""""process_name"\s*:\s*"({process_name}[^"]+)""""
""""(process_)?path"\s*:\s*"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))""""
""""observed_filename"\s*:\s*\[?"({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))""""
""""process_guid":"({process_guid}[^"]+)"""
""""ioc_attr"\s*:\s*"({ioc}([^"\\]|(\\\\)*\\"|\\)+)""""
""""ioc_value"\s*:\s*"({ioc}[^"]+)""""
""""parent_guid"\s*:\s*"({parent_process_guid}[^"]+)"""
""""parent_name"\s*:\s*"({parent_process}[^"]+)"""
""""cmdline"\s*:\s*"\\?"({process_command_line}[^"]+?)\\?""""
""""host_type"\s*:\s*"({host_type}[^"]+)""""
]
DupFields = [
"process_path->path"
]
SOAR {
  IncidentType = "generic"
  DupFields = [
"""time->startedDate"""
"""vendor->source"""
"""rawLog->sourceInfo"""
"""alert_name->description"""
"""alert_severity->sourceSeverity"""
  ]
  NameTemplate = "Carbon Black Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
"""dest_ip->ip_address"""
"""dest_host->host_name"""
      ]
    

}
```