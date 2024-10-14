#### Parser Content
```Java
{
Name = "fireeye-emailsecurity-cef-alert-trigger-success-fireeye"
Vendor = "FireEye"
Product = "FireEye CMS"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """CEF:"""
  """|FireEye|"""
  """flexString2Label=subject"""
  """|CMS|"""
  """fileType="""
]
Fields = [
  """rt=({time}[a-zA-Z]{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """act=({action}[^=]+?)\s*\w+="""
  """externalId=({alert_id}\d+)"""
  """\|FireEye\|([^\|]+\|){3}({alert_name}[^\|]+)\|"""
  """\scs1Label=sname cs1=({alert_name}[^\s]+)"""
  """\|FireEye\|([^\|]+\|){3}({alert_type}[^\|]+)\|({alert_severity}[^\|]+)\|"""
  """\sdhost=({dest_host}\S+)"""
  """\scs5Label=cncHost cs5=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s]+))"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sfname=(?:[^,]+,)?\s*({file_name}.+?)\s*(?:\w+=|$)"""
  """\sfname=({file_name}[^=]+?)\s*(?:\w+=|$)"""
  """\sdvc=({host}[A-Fa-f:\d.]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^\s]+)?\s+cn1Label"""
  """\sduser=({email_address}[^@\s]+@[^,\s]+)"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_type->malwareCategory"
    "alert_severity->sourceSeverity"
    "src_host->malwareVictimHost"
    "malware_file_name->malwareAttackerFile"
    "malware_url->malwareAttackerUrl"
    "dest_ip->malwareAttackerIp"
  ]
  NameTemplate = "FireEye Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
        "src_host->host_name"
      ]
    

}
```