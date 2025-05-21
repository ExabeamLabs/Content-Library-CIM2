#### Parser Content
```Java
{
Name = "pan-ngfw-csv-alert-trigger-success-data"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [
  """,THREAT,data,"""
]
Fields = [
  """THREAT,({alert_type}[^,]+),[^,]*,({time}\d\d\d\d/\d\d/\d\d \d\d:\d\d:\d\d),({src_ip}[\da-fA-F\.:]+),({dest_ip}[\da-fA-F\.:]+)(,|$)"""
  """THREAT,data,([^,]*,){25}({action}[^,]+)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){27}({device_name}({host}[\w\-\.]+))(,|$)"""
  """THREAT,data,([^,]*,){8}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(|({domain}[^\\,]+))\\?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(,|$)"""
  """THREAT,data,([^,]*,){7}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(|({domain}[^\\,]+))\\?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(,|$)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),({alert_name}[^,]+)(,|$)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){4}({alert_id}\d+)(,|$)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){2}({alert_severity}[\w\-\.]+)(,|$)""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
  """,THREAT,([^,]*,){29}({category}[^,]*),"""
  """THREAT,([^,]*,){4}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?,""",
  """THREAT,([^,]*,){5}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_translated_port}\d+))?,""",
  """THREAT,([^,]*,){10}(not-applicable|({network_app}[^,]+)),""",
  """THREAT,([^,]*,){12}({src_network_zone}[^,]+),""",
  """THREAT,([^,]*,){13}({dest_network_zone}[^,]+),""",
  """THREAT,([^,]*,){14}({src_interface}[^,]+),""",
  """THREAT,([^,]*,){15}({dest_interface}[^,]+),""",
  """({serial_num}[^,]+),THREAT,"""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_severity->sourceSeverity"
    "alert_id->sourceId"
    "src_ip->malwareVictimHost"
    "alert_type->malwareCategory"
    "dest_ip->malwareAttackerIp"
    "action->description"
 ]
  NameTemplate = "Palo Alto Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "src_address"
      Fields = [
        "src_ip->ip_address"
      ]
    

}
```