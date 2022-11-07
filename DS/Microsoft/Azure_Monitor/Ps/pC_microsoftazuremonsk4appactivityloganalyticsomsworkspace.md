#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-app-activity-loganalyticsomsworkspace
  ParserVersion = v1.0.0
  Product = Azure Monitor
  Conditions = [ """destinationServiceName =Azure""", """dproc=Log Analytics OMS Workspace""" ]

cef-cloud-system-info = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)""",
    """destinationServiceName =({app}[^=]+?)\s+(\w+=|$)""",
    """dproc=({process_name}[^=]+?)\s+(\w+=|$)""",
# log_level is removed
    """"TenantId":"({tenant_id}[^"]+)""",
    """"Hostname_s":"({host}[^"]+)""",
# src_system is removed
    """"Type":"({event_category}[^"]+)""",
    """"Computer":"({computer_name}[^"]+)""",
# mg is removed
    """"ManagementGroupName":"({group_name}[^"]+)""",
    """"_ResourceId":"({resource_id}[^"]+)""",
# code_cf is removed
    """"ClusterName_s":"({cluster_name}[^"]+)""",
# cluster_type is removed
# full_log is removed
    """Activity":"({event_name}[^"]+)""",
    """message":"({event_name}[^"]+)""",
    """errorCode":"({error_code}[^"]+)""",
# full_log is removed
    """"Message":"\[({event_name}[^\]]+)""",
    """"\$table":"({table}[^"]+)""",
    """User Agent - ({user_agent}.+?)\s+\[""",
    """"sourceIPs":\["({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
    """"userAgent":"({user_agent}[^"]+)"""",
    """"code":({response_code}\d+)""",
    """"AlertSeverity":"({alert_severity}[^",]+)""",
    """"AlertName":"({alert_name}[^",]+)""",
    """"RiskScore"+:\s*"+({alert_severity}[^",]+)"""
  ]
 }


}
#============================================== Start of DefaultWeakParsersAA  section ==================================================================
DefaultWeakParsers = [
{
Name = "honeywell-pw-json-physical-location-access-areaname"
Vendor = "Honeywell"
Product = "Honeywell Pro-Watch"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"fielddatetime":""""
  """"areaname":""""
  """"cardholderid":"""
  """"locationfullname":""""
  """"cardholderfirstname":""""
]
Fields = [
  """"fielddatetime\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
  """"source\":\"({src_host}[\w\-.]+)"""
  """"category\":({category}\d+)"""
  """"eventid\":({event_code}\d+)"""
  """"cardholderid\":({badge_id}\d+)"""
  """"areacode\":({area_code}\d+)"""
  """"description\":\"({additional_info}[^\"]+)"""
  """"accessreason\":\"({action}[^\"]+)"""
  """"locationfullname\":\"({location_full}[^\"]+)"""
  """"areaname\":\"({location_area}[^\"]+)"""
  """"cardnumber\":\"({card_num}[^\"]+)"""
  """"cardholderfirstname\":\"({first_name}[^\"]+)"""
  """"cardholderlastname\":\"({last_name}[^\"]+)"""
  """"zoneentered\":\"({location_door}[^\"]+)"""
]
DupFields = [
  "location_area->location_building"
]
ParserVersion = "v1.0.0"
},
{
Name = "badge-b-json-physical-location-access-fail-badge"
Vendor = "Badge"
Product = "Badge"
TimeFormat = "epoch_sec"
Conditions = [
  """BADGE"""
  """Floor"""
]
Fields = [
  """(?:([^\|]*\|))\s+({time}\d+)"""
  """(?:([^\|]*\|)){3}\s+({last_name}[^,\|]+),\s+({first_name}[^\|]+)\s+\|"""
  """(?:([^\|]*\|)){4}\s+({action}[^\|]+)\s+\|"""
  """(?:([^\|]*\|)){5}\s+\d+\s+-\s*({location_city}[^-]+)\s+-({location_door}[^\|]+)\s+\|"""
  """(?:([^\|]*\|)){6}\s+({location_building}.+?)\s+$"""
]
ParserVersion = "v1.0.0"
},
{
Name = "pictureperfect-pp-str-physical-location-access-success-pp"
Vendor = "PicturePerfect"
Product = "PicturePerfect"
TimeFormat = "yyyyMMdd|HHmmss"
Conditions = [
  """pictureperfect"""
]
Fields = [
  """^[^|]*?\|([^|]*\|){2}({user}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){3}({first_name}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){4}({last_name}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){12}({location_full}[^|]+)\|"""
  """^[^|]*?\|([^|]*\|){12}[^|]*\s({direction}(?:IN|OUT))\s[^|]*\|"""
  """^[^|]*?\|([^|]*\|){15}({time}\d{8}\|\d{6})\|"""
]
DupFields = [
  "location_full->location_door"
]
ParserVersion = "v1.0.0"
},
{
  Name = "xps-x-cef-print-activity-printer-activity-success-xpsprint"
  Vendor = "XPS"
  Product = "XPS"
  TimeFormat = "yyyy-MM-dd        HH:mm:ss a"
  Conditions = [
    """XPS"""
    """ PRINT"""
  ]
  Fields = [
    """({time}\d+\-\d+\-\d+\s+\d+:\d+:\d+ (PM|pm|AM|am))\s+({host}[^\s]+)\s+(?:-|({printer_name}[^\s]+))\s+\d+\s+(?:-|({user}[^\s]+))\s+[^\s]+\s+(?:-|({src_host}[^\s]+))\s+(?:-|({object}.+?))\s(\d*\s*){3}\d+\.\d+\s+.+?\s+(\d+\s+){3}XPS\s+({operation}PRINT)""" 
 ]
  DupFields = [
    "printer_name->dest_host"
  ]
  ParserVersion = "v1.0.0"
},
{
  Name = okta-amfa-csv-app-login-fail-signfailed
  ParserVersion = v1.0.0
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """,Sign-""", """n Failed """]
  Fields = [
    """([^,]*,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """Sign-(i|I)n Failed.*?([^,]*,){3}({src_ip}[^,]+)""",
    """Verification failed for user:\s*(({email_address}[^"@]+@[^"@]+)|({user}[^"]+))"*,""",
    """([^,]*,){4}(({email_address}[^,@]+@[^,@]+)|({user}[^,]+))""",
    """Sign-(i|I)n Failed\s*-\s*({failure_reason}[^:",]+)""",
    """([^,]*,){11}\/app\/({app}[^\/]+)""",
  ]
  DupFields = ["src_file_path->file_dir"
}
```