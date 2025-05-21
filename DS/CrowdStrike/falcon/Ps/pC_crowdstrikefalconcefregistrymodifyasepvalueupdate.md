#### Parser Content
```Java
{
Name = "crowdstrike-falcon-cef-registry-modify-asepvalueupdate"
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_simpleName":"AsepValueUpdate"""" ]
  Fields = ${DLCrowdStrikeParserTemplates.cef-crowdstrike-app-activity-temp-dl.Fields} [
    """"RegObjectName":"({registry_path}[^"]*?({registry_key}[^"\\]+))"""",
    """"RegValueName":"({registry_value}[^"]+?)"""",
    """({operation}Update)""",
    """({object}AsepValue)""",
    """"cid":"({cid}[^"]+)"""
    """"RegStringValue":"({registry_details}[^"]+)"""",
    """exa_json_path=$.cid,exa_field_name=cid"""
    """exa_json_path=$.RegObjectName,exa_regex=^({registry_path}[^"]*?({registry_key}[^"\\]+))$""",
    """exa_json_path=$.RegValueName,exa_field_name=registry_value"""
    """exa_regex=({operation}Update)""",
    """exa_regex=({object}AsepValue)""",
    """exa_json_path=$.RegStringValue,exa_field_name=registry_details"""
  ]

cef-crowdstrike-app-activity-temp-dl = {
  Vendor = "CrowdStrike"
  Product = "Falcon"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Fields = [
    """"timestamp":\s*"*({time}\d{10})""",
    """"UserIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WdestinationServiceName =({app}.+?)\s+\w+="""
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"aid":\s*"({aid}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """"UserName":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
    """exa_regex=\WdestinationServiceName =({app}.+?)\s+\w+="""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.UserIp,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_regex="(ImageFileName|TargetFileName)":\s*"({file_path}[^"]+)""",
    """exa_regex=(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
    """exa_regex="UserName":"(({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """exa_regex="aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """exa_json_path=$.name,exa_field_name=alert_type""",
    """exa_json_path=$.ClientComputerName,exa_field_name=src_host""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
  
}
```