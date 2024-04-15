#### Parser Content
```Java
{
Name = "microsoft-defenderep-json-file-success-tenantid"
Conditions = [
""""Type":"AdvancedHuntingDeviceFileEvents_CL"""
"""TimeGenerated"""
"""TenantId"""
]
ParserVersion = "v1.0.0"

cef-sysmon-file-write = {
    Vendor = Microsoft
    Product = Sysmon
    TimeFormat = "epoch"
    Fields = [
      """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
      """({host}\S+) CEF:""",
      """\Wdvc=({host}[A-Fa-f:\d]+)""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """\Wrt=({time}\d{13})""",
      """\WeventId=({event_code}\d+)""",
      """\WcategoryOutcome=\/({result}.+?)\s+(\w+=|$)""",
      """\Wdproc=({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s+(\w+=|$)""",
      """\Wdproc=({process_path}({process_dir}.*?)({process_name}[^\\]+?))\s+(\w+=|$)""",
      """\Wfname=.+?USERS\\+({user}[^\s\\]+)""",
      """\Wfname=({file_path}({file_dir}.*?)({file_name}[^\\.]+(\.({file_ext}[^\\.]+?))?))\s+(\w+=|$)""",
      """\Wcs6=\{({process_guid}[^\}]+)""",
      """\Wdpid=({process_id}\d+)""",
      """\Wcs1=({object}.+?)\s+(\w+=|$)""",
    ]
    DupFields = [ "host->dest_host" 
}
```