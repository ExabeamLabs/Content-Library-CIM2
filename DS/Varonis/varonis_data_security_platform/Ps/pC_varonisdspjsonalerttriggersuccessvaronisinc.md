#### Parser Content
```Java
{
Name = "varonis-dsp-json-alert-trigger-success-varonisinc"
 Vendor = "Varonis"
 Product = "Varonis Data Security Platform"
 TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [
  """|Varonis Inc.|"""
  """|DatAdvantage|"""
  """cat=Alert"""
 ] 
Fields = [
   """\|rt=({time}\w{3} \d+ \d\d\d\d \d\d:\d\d:\d\d)"""
   """({host}[\w.\-]+)\s+CEF:"""
   """\d\d:\d\d\s({host}[^\s]+)\sVaronis-DatAlert:"""
   """\sdvc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
   """\sdvchost=(?:|({dest_ip}\d+\.\d+\.\d+\.\d+)|({dest_host}[\w\-.]+))\s\w+="""
   """\sduser=(?:|((Abstract|({domain}[^\\]+))\\+)?(Nobody|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+="""
   """\sduser=(?:|((Abstract|({domain}[^\\]+))\\+)?(Nobody|SYSTEM|({full_name}[^\\\s,=]+\s+[^\\,=]+?)))\s+\w+="""
   """\sduser=(?:|(({domain}[^\\]+)\\+)?({last_name}[^\\,=]+?),\s*({first_name}[^\\,=]+))\s+\w+="""
   """\|Varonis Inc.\|([^|]*\|){3}({access}[^|]+)\|"""
   """\Wact=({access}[^=]+?)\s+(\w+=|$)"""
   """\scs2=\s*(?:|({alert_name}.+?))(\s+likely|\s+\w+=)"""
   """\sfilePath=(?:|({additional_info}.+?))\s+\w+="""
   """\s(fname|filePath)=({file_path}({file_dir}[^=]*?[\\\/]+)?({file_name}[^\\\/=]+?(\.({file_ext}\w+))?))\s+\w+="""
   """\sdhost=(?:|({dest_ip}\d+\.\d+\.\d+\.\d+)|({dest_host}[\w\-.]+))\s+\w+="""
   """\soutcome=(?:|({result}\S+?))\s+\w+="""
   """\|Varonis Inc.\|([^\|]+\|){4}({alert_severity}\d+)\|"""
   """SAMAccountName =(SYSTEM|not available|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
 ]
 DupFields = [
  "alert_name->alert_type"
]
SOAR {
  IncidentType = "dlp"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_type->description"
    "user->dlpUser"
    "alert_name->dlpPolicy"
    "file_name->dlpFileName"
    "host->dlpDeviceName"
  ]
  NameTemplate = "Varonis DLP Alert ${alert_name} found"
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