#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-json-alert-trigger-success-feed"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch_sec"
Conditions = [
  """"type":"feed."""
  """"cb_server":""""
]
Fields = [
  """"timestamp\"\s*:\s*\"?({time}\d{10})"""
  """"hostname\"\s*:\s*\"({host}[^\s\"]+)""""
  """"type\"\s*:\s*\"({alert_type}[^\"]+)""""
  """"computer_name\"\s*:\s*\"({dest_host}[^\"]+)""""
  """"interface_ip\"\s*:\s*\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"username\"\s*:\s*\"(({domain}[^\\\"]+)\\+)?({user}[^\\\s\"]+)"""
  """"sensor_id\"\s*:\s*\"?({sensor_id}[^\",]+)"""
  """"process_md5\"\s*:\s*\"({hash_md5}[^\"]+)\""""
  """"unique_id\"\s*:\s*\"\{?({alert_id}[^\}\"]+)"""
  """"os_type\"\s*:\s*\"({os}[^\"]+)"""
  """"process_name\"\s*:\s*\"({process_name}[^\"]+)""""
  """"path\"\s*:\s*\"({process_path}({process_dir}([^\"]+)?[\\\/])?({process_name}[^\\\/\"]+))""""
  """"process_guid\"\s*:\s*\"({process_guid}[^\"]+)""""
  """"ioc_query_string\"\s*:\s*\"({ioc}.+?)\","""
  """"parent_guid\"\s*:\s*\"({parent_process_guid}[^\"]+)"""
  """"parent_name\"\s*:\s*\"({parent_process}[^\"]+)"""
  """"cmdline\"\s*:\s*\"\\?\"({process_command_line}[^\"]+?)\\?""""
  """"host_type\"\s*:\s*\"({host_type}[^\"]+)""""
]
DupFields = [
  "process_path->path"
  "ioc->alert_name"
]
SOAR {
  IncidentType = "generic"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->description"
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