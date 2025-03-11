#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-scheduled-task-modify-win
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":""", """"ScheduledTaskModified"""", """"event_platform":""", """"Win""""]
  Fields = ${CrowdStrikeParsersTemplates.cef-crowdstrike-app-activity-temp-aa.Fields} [
    """"TaskName":\s*"({task_name}[^"]+)"""
    """"TaskExecCommand":\s*"({file_path}[^"]+)""",
    """"TaskExecCommand":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"TaskExecArguments":\s*"\s*({additional_info}[^"]+?)\s*""""
    """"cid":"({cid}[^"]+)"""

  ]

cef-crowdstrike-app-activity-temp-aa = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Fields = [
    """"timestamp":\s*"*({time}\d{10})""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WdestinationServiceName =({app}.+?)\s+\w+="""
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
    """"event_platform":"({os}[^"]+)""""
    """exa_regex=\WdestinationServiceName =({app}.+?)\s+\w+="""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_regex="(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """exa_regex="(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """exa_regex="UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """exa_regex="aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """exa_json_path=$.name,exa_field_name=alert_type""",
    """exa_json_path=$.ClientComputerName,exa_field_name=src_host""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
  
}
```