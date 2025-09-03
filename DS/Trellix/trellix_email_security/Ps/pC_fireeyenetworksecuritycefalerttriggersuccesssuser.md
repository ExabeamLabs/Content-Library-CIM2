#### Parser Content
```Java
{
Name = "fireeye-networksecurity-cef-alert-trigger-success-suser"
Vendor = "Trellix"
Product = "Trellix Email Security"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|eMPS"""
  """suser="""
]
Fields = [
  """\|(FireEye|Trellix)\|([^|]*\|){3}({alert_type}[^|]+)"""
  """\|(FireEye|Trellix)\|([^|]*\|){4}({alert_severity}[^|]+)"""
  """\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\WfilePath=({additional_info}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wrequest=({malware_url}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wcs5=({malware_url}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wdvc=(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))"""
  """\Wdvchost=({host}[\w\-\.]+)(\s+\w+=|\s*$)"""
  """\Wsuser=({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wduser=({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wduser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\Wcn2=({alert_id}\d+)"""
  """\Wcs1=({alert_name}[^=]+?)(\s+\w+=|\s*$)"""
  """\Wsproc=({process_name}[^=]+?)(\s+\w+=|\s*$)"""
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
    "dest_user->user"
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