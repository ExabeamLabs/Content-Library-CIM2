#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-kv-alert-trigger-success-execution"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
"""Cb Protection event:"""
"""subtype="Execution block"""
""" process="""
]
Fields = [
"""({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
"""\sdate="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|PM|pm))"""
"""\stext="({additional_info}[^"]+)""""
"""\ssubtype="({event_code}[^"]+)""""
"""\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)""""
"""\susername="(({domain}[^"\\]+)\\)?({user}[\w\.\-]{1,40}\$?)""""
"""\sip_address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sprocess="({process_path}(({process_dir}[^"]+?)\\)?({process_name}[^"\\]+?))""""
"""\sfile_hash="({hash_md5}[^"]+)""""
"""\srule_name="({alert_name}[^"]+)""""
"""\sprocess_threat="({alert_severity}[^"]+)""""
"""\sfile_hash="({hash_md5}[^"]+)""""
"""\sfile_path="({file_path}[^"]+)""""
"""\sfile_name="({file_name}[^"]+)""""
]
DupFields = [
"event_code->alert_type"
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