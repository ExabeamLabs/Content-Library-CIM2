#### Parser Content
```Java
{
Name = "fireeye-networksecurity-cef-alert-trigger-success-deviceseverity"
Vendor = "FireEye"
Product = "FireEye CMS"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|FireEye|"""
""" deviceSeverity="""
]
Fields = [
"""\|FireEye\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_type}[^|]+?)\|"""
"""\|FireEye\|[^|]+?\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|"""
"""\sdeviceSeverity=({alert_severity}\d+)"""
"""\sexternalId=({alert_id}[^\s]+)"""
"""\srt=({time}\d{13})"""
"""\|FireEye\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sshost=({src_host}[^\s]+)"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""\scs1Label=sname cs1=({alert_name}.+?) """
"""\scs1=({alert_name}.+?)\s+\w+=.*?cs1Label=sname"""
"""\scs5Label=cncHost cs5=({malware_url}.+?) """
"""\srequest=({malware_url}.+?) """
"""\sfname=({malware_url}.+?) """
"""\sduser=<?({user}[^@]+)(@[^\s]+)?\s+\w+="""
"""\ssuser=({additional_info}.+?)\s+\w+="""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""proto=({protocol}[^\s]+)"""
"""smac=({src_mac}[^\s]+)"""
"""dmac=({dest_mac}[^\s]+)"""
"""spt=({src_port}\d+)"""
"""fileHash=({file_hash}[^\s]+)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
"time->startedDate"
"vendor->sou"
    {
      EntityType = "device"
      Name = "dest_address"
      Fields = [
"dest_ip->ip_address"
"dest_host->host_name"
      ]
    

}
```