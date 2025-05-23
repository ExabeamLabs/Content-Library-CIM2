#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-alert-trigger-success-host"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
"""CEF"""
"""|CrowdStrike|FalconHost|"""
]
Fields = [
"""\srt=({time}\d{10})"""
"""({host}[\w.\-]+) CEF:"""
"""\s({host}[^\s]+)\s+CrowdStrike Falcon"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""(\s|\|)(s|d)ntdom=(?:N\/A|({domain}[^\s]+))"""
"""(\s|\|)suser=(?:N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}.+?))?\s+(\w+=|$)"""
"""(\s|\|)duser=(?:N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(@({domain}.+?))?\s+(\w+=|$)"""
"""(\s|\|)dhost=({src_host}[^\s]+)"""
"""(\s|\|)shost=({src_host}[^\s]+)"""
"""(\s|\|)shost=.+?(\s|\|)dhost=({dest_host}[^\s]+)"""
"""(\s|\|)dhost=({dest_host}[^\s]+).+?(\s|\|)shost="""
"""(\s|\|)src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""(\s|\|)dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""CrowdStrike\|([^|]+\|){3}({alert_name}[^|]+)"""
"""CrowdStrike\|([^|]+\|){2}({alert_type}[^|]+)"""
"""CrowdStrike\|([^|]+\|){4}({alert_severity}[^|]+)"""
"""(\s|\|)cat=({alert_name}.+?)\s+(\w+=|$)"""
"""(\s|\|)cs3=({alert_name}.+?)\s+\w+=.*?cs3Label=ScanResultName"""
"""cs3Label=ScanResultName.*?cs3=({alert_name}.+?)\s+(\w+=|$)"""
"""(\s|\|)cs1=({alert_name}.+?)\s+\w+=.*?cs1Label=ScanResultName"""
"""cs1Label=ScanResultName.*?cs1=({alert_name}.+?)\s+(\w+=|$)"""
"""(\s|\|)msg=({additional_info}.+?)\s+(\w+=|$)"""
"""(\s|\|)fname=({file_name}.+?)\s+(\w+=|$)"""
"""(\s|\|)filePath=({file_path}.+?)\s+(\w+=|$)"""
"""(\s|\|)cs1=("+)?({process_command_line}.+?)("+)?\s\w+=.*(?=cs1Label=CommandLine)"""
"""(?=cs1Label=CommandLine).*cs1=("+)?({process_command_line}.+?)("+)?\s+(\w+=|$)"""
"""(\s|\|)cs5=("+)?({process_command_line}.+?)("+)?\s\w+=.*(?=cs5Label=CommandLine)"""
"""(?=cs5Label=CommandLine).*cs5=("+)?({process_command_line}.+?)("+)?\s+(\w+=|$)"""
"""(\s|\|)cs6=({falcon_host_link}.+?)\s\w+=.*(?=cs6Label=FalconHostLink)"""
"""(?=cs6Label=FalconHostLink).*cs6=({falcon_host_link}.+?)\s+(\w+=|$)"""
]
DupFields = [ "falcon_host_link->additional_info", "file_name->process_name", "file_path->process_dir" ]
ParserVersion = "v1.0.0"


}
```