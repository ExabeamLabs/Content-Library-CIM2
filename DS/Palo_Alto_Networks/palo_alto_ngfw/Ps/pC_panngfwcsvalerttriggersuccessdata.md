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
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){27}({host}[\w\-\.]+)(,|$)"""
  """THREAT,data,([^,]*,){8}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(|({domain}[^\\,]+))\\?(|({user}[\w\.\-]{1,40}\$?)))(,|$)"""
  """THREAT,data,([^,]*,){7}(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(|({domain}[^\\,]+))\\?(|({user}[\w\.\-]{1,40}\$?)))(,|$)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),({alert_name}[^,]+)(,|$)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){4}({alert_id}\d+)(,|$)"""
  """THREAT,data,([^,]*,){26}(("*[^"]*")|[^,]*),([^,]*,){2}({alert_severity}[\w\-\.]+)(,|$)""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
  """,THREAT,([^,]*,){29}({category}[^,]*),"""
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