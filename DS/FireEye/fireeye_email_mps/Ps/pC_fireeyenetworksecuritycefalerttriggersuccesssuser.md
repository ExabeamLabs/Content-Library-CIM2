#### Parser Content
```Java
{
Name = "fireeye-networksecurity-cef-alert-trigger-success-suser"
Vendor = "FireEye"
Product = "FireEye Email MPS"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|FireEye|eMPS"""
  """suser="""
]
Fields = [
  """\|FireEye\|([^|]*\|){3}({alert_type}[^|]+)"""
  """\|FireEye\|([^|]*\|){4}({alert_severity}[^|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\WfilePath=({additional_info}.+?)(\s+\w+=|\s*$)"""
  """\Wrequest=({malware_url}.+?)(\s+\w+=|\s*$)"""
  """\Wcs5=({malware_url}.+?)(\s+\w+=|\s*$)"""
  """\Wdvc=({host}\d+\.\d+\.\d+\.\d+)"""
  """\Wdvchost=({host}.+?)(\s+\w+=|\s*$)"""
  """\Wsuser=({src_user}[^@\s]+)"""
  """\Wduser=({dest_user}[^@\s]+)"""
  """\Wduser=({email_address}[^@\s,]+@[^@\s,]+)"""
  """\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wcn2=({alert_id}\d+)"""
  """\Wcs1=({alert_name}.+?)(\s+\w+=|\s*$)"""
  """\Wsproc=({process_name}.+?)(\s+\w+=|\s*$)"""
  """\Wact=({action}[^=]+?)\s+\w+="""
]
SOAR {
  IncidentType = "malware"
  DupFields = [
    "time->startedDate"
    "vendor->source"
    "rawLog->sourceInfo"
    "alert_name->malwareName"
    "alert_id->sourceId"
    "alert_type->malwareCategory"
    "alert_severity->sourceSeverity"
    "malware_url->malwareAttackerUrl"
  ]
  NameTemplate = "FireEye Alert ${alert_name} found"
  ProjectName = "SOC"
  EntityFields = [
    {
      EntityType = "device"
      Name = "url"
      Fields = [
        "malware_url->url"
      ]
    

}
```