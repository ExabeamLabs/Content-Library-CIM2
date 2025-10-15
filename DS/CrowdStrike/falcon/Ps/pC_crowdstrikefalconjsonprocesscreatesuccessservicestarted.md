#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-process-create-success-servicestarted
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "epoch"
  Conditions = [ 
""""event_simpleName":""""
"""ServiceStarted""" 
]
  Fields = [
    """"timestamp":\s*"({time}\d{13})"""",
    """"CommandLine":\s*"({dest_process_command_line}({parent_process_command_line}({process_command_line}.+?)))\s*","TargetProcessId""",
    """"name":\s*"({service_name}[^"]+)""",
    """"ServiceDisplayName":"({service_name}[^"]+)"""",
    """"event_simpleName":\s*"({event_code}[^"]+)""",
    """"UserName":\s*"((LOCAL SERVICE|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))))"""",
    """"UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """src-account-name":"({account_name}[^"]+)""",
    """"ImageFileName":\s*"[\\\?]+(|({parent_process_path}({parent_process_dir}[^"]*?)(\\+({parent_process_name}[^"\\]+?))?))""""
    """"aid":\s*"({aid}[^"]+)""",
    """"event_platform":\s*"({os}[^"]+)"""
    """"InterfaceGuid":"({process_guid}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
    """"ImageFileName":\s*"[\\\?]+(|({dest_process_path}({process_path}({dest_process_dir}({process_dir}[^"]*?))(\\+({dest_process_name}({process_name}[^"\\]+?)))?)))""""
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"ComputerName":"({host}[\w\-\.]+)""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_regex="timestamp":\s*"({time}\d{13})"""",
    """exa_json_path=$.CommandLine,exa_field_name=process_command_line""",
    """exa_json_path=$.CommandLine,exa_field_name=parent_process_command_line""",
    """exa_json_path=$.CommandLine,exa_field_name=dest_process_command_line""",
    """exa_json_path=$.name,exa_field_name=service_name""",
    """exa_json_path=$.ServiceDisplayName,exa_field_name=service_name""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.UserName,exa_regex=((LOCAL SERVICE|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))))""",
    """exa_json_path=$.UserName,exa_regex=(LOCAL SERVICE|(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_regex="ImageFileName":\s*"[\\\?]+(|({parent_process_path}({parent_process_dir}[^"]*?)(\\+({parent_process_name}[^"\\]+?))?))"""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.InterfaceGuid,exa_field_name=process_guid""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_regex="ImageFileName":\s*"[\\\?]+(|({dest_process_path}({process_path}({dest_process_dir}({process_dir}[^"]*?))(\\+({dest_process_name}({process_name}[^"\\]+?)))?)))""""
    """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
    """exa_json_path=$.aip,exa_field_name=aip"""
  ]


}
```