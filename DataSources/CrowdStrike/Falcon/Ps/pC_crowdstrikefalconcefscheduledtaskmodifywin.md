#### Parser Content
```Java
{
Name = crowdstrike-falcon-cef-scheduled-task-modify-win
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":""", """"ScheduledTaskModified"""", """"event_platform":""", """"Win""""]
  Fields = ${CrowdStrikeParsersTemplates.cef-crowdstrike-app-activity-temp-dl.Fields} [
    """"TaskName":\s*"({task_name}[^"]+)"""
    """"TaskExecCommand":\s*"({file_path}[^"]+)""",
    """"TaskExecCommand":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"TaskExecArguments":\s*"\s*({additional_info}[^"]+?)\s*""""

  ]

cef-crowdstrike-app-activity-temp-dl = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":\s*"*({time}\d{10})""",
    """"UserIp":\s*"({src_ip}[^"]+)""",
    """\WdestinationServiceName =({app}.+?)\s+\w+="""
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"UserName":\s*"({user}[^"]+?)""""
    """"aip":\s*"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
  
}
```