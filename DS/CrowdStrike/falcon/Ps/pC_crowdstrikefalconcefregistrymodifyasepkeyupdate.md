#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-registry-modify-asepkeyupdate"
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":"AsepKeyUpdate"""" ]
  Fields = ${DLCrowdStrikeParserTemplates.cef-crowdstrike-app-activity-temp-dl.Fields} [
    """"RegObjectName":"({registry_key}[^"]+)""",
    """"RegStringValue":"({registry_value}[^"]+)""",
    """({access}Update)""",
    """({object}AsepKey)"""
  ]
  DupFields = [registry_key -> registry_path]

cef-crowdstrike-app-activity-temp-dl = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch_sec"
  Fields = [
    """"timestamp":\s*"*({time}\d{10})""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WdestinationServiceName =({app}.+?)\s+\w+="""
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"UserName":\s*"({user}[^"]+?)""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
  
}
```