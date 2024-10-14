#### Parser Content
```Java
{
Name = "fireeye-endpointsecurity-cef-alert-trigger-success-fireeyeacquisitionerror"
Conditions = [
  """|fireeye|hx|"""
  """|FireEye Acquisition Error"""
  """categoryTupleDescription="""
  """CEF:"""
]
ParserVersion = "v1.0.0"

fireeye-eps-hx-alert = {
  Vendor = FireEye
  Product = FireEye Endpoint Security (HX)
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """\Wrt=({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)"""
    """\|fireeye\|([^\|]*\|){2}({alert_type}.+?)\|"""
    """\|fireeye\|([^\|]*\|){3}({alert_name}.+?)\|"""
    """\|fireeye\|([^\|]*\|){4}({alert_severity}.+?)\|"""
    """\WexternalId=({alert_id}\d+)"""
    """\Wdntdom=(?:NA|({domain}.+?))(\s+\w+=|\s*$)"""
    """\Wdst=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\Wsuser=(({email_address}[^\s@]+@[^\s\.]+\.[^\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+="""
    """\Wdhost=({src_host}[^\s]+)"""
    """\Wdvchost=({host}[^\s]+)"""
    """\Wmsg=({additional_info}.+?)\s+\w+="""
    """act=({action}[^=]+?)\s\w+="""
    """\srequest=({malware_url}.+?)\s\w+="""
    """filePath=({file_path}(({file_dir}[^=]+[^\\\/])[\\\/]+)?({file_name}[^=\\\/]+?))\s+(\w+=|$)"""
    """fname=({file_name}[^=]+?(\.({file_ext}[^=\.]+?))?)\s\w+="""
    """categoryOutcome=\/*({result}[^=]+?)\s\w+=""",
    """cs4Label=Process Name.*?cs4=({process_path}({process_dir}[^\.]+?)\\+({process_name}[^\\]+?))\s*(\w+=|$)"""
  ]
  DupFields = ["file_name->malware_file_name"]
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
  
}
```