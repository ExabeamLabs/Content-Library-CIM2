#### Parser Content
```Java
{
Name = "tripwire-t-str-alert-trigger-success-modifyfile"
Vendor = "Tripwire Enterprise"
Product = "Tripwire Enterprise"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""TRIPWIRE"""
""" Modify:"""
""" on """
""" by """
]
Fields = [
"""\s({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})\s"""
"""(\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})\s({host}[^\s]+?)\sModify:"""
"""\s+Modify:\s+({access}[A-Za-z]+?)\s+"""
"""\sModified\s({file_path}[^|]+?)\son\s"""
"""\sModified\s({file_dir}[^|]+?)[\\\/]+[^\\\/]+\son\s"""
"""\sModified\s([^|]*?[\\\/]+)?({file_name}[^\\\/|]+)\son\s"""
"""\sModified\s[^|]+?[\\\/]+[^\\\/|.]+\.({file_ext}[^\\\/|]+)(\son\s)"""
"""\son\s({dest_host}[^\s]+?)\sby\s"""
"""\sby\s({alert_name}.+?)\s*$"""
"""({alert_type}Modify)"""
]
SOAR {
  IncidentType = "generic"
  DupFields = [
"time->startedDate"
"vendor->source"
"rawLog->sourceInfo"
"alert_type->description"
  ]
  NameTemplate = "Tripwire Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
"dest_host->host_name"
      ]
    

}
```