#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-alert-trigger-success-securityplatform-1
Vendor = VMware
Product = Carbon Black App Control
TimeFormat = "MM dd yyyy HH:mm:ss"
Conditions = [
  """|Bit9|Security Platform|"""
  """|Carbon Black watchlist|"""
]
Fields = [
  """({time}\d\d \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """(\||\s)cs5=(|({alert_name}.+?))\s+([\w-]+=|$)"""
  """(\||\s)externalId=({alert_id}.+?)(\s+[\w-]+=|\s*$)"""
  """(\||\s)cat=(|({alert_type}.+?))\s+(\w+=|$)"""
  """(\||\s)deviceProcessName =({process_path}.+?)\s+?([\w-]+=|$)"""
  """(\||\s)deviceProcessName =.+?({process_name}[^\\]+?)\s+([\w-]+=|$)"""
  """(\||\s)deviceProcessName =({process_dir}.+?)\\+[^\\]+\s+([\w-]+=|$)"""
  """(\||\s)dst=(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)(\s+[\w-]+=|\s*$)"""
  """(\||\s)dhost=(|(\S+\\+)?({dest_host}.+?))\s+(\w+=|$)"""
  """(\||\s)duser=(|(({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """(\||\s)dvchost=(|({host}.+?))(\s\w+=|\s*$)"""
  """(\||\s)msg=.+?for process\s+'.+?'\s+\[({hash_md5}[a-fA-F0-9]+)\]"""
  """(\||\s)sproc=({process_guid}.+?)(\s+[\w-]+=|\s*$)"""
]
DupFields = [
  "process_path->path"
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
        """dest_ip->ip_address"""
        """dest_host->host_name"""
      ]
    

}
```