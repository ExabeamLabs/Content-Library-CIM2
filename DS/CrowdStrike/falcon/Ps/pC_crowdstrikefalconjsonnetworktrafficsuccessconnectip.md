#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-network-traffic-success-connectip
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ 
""""event_simpleName":"NetworkConnectIP""" 
]
  Fields = [
    """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
    """hostname":"({host}[^"]+)"""",
    """"timestamp":\s*"*({time}\d{13})"""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"name":"({event_name}[^"]+)"""",
    """"LocalAddressIP(4|6)":"(0:0:0:0:0:0:0:0|0.0.0.0|127.0.0.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"RemoteAddressIP(4|6)":"(0:0:0:0:0:0:0:0|0.0.0.0|127.0.0.1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"LocalPort":"({src_port}\d+)""",
    """"RemotePort":"({dest_port}\d+)""",
    """"ConnectionDirection":"({direction}(0|1))""",
    """"Protocol":"({protocol}[^"]+)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"ContextProcessId":"({process_guid}[^"]+)"""",
    """"aip":\s*"({aip}[^"]+)"""",
    """ConnectionDirection":"({direction}1)",.+?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","LocalPort":"*({dest_port}\d+)"*,.+?"RemoteAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*"*({=src_port}\d+)"""",
    """ConnectionDirection":"({direction}0)",.+?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","LocalPort":"*({src_port}\d+)"*,.+?"RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*"*({=dest_port}\d+)"""",
    """"LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
   """"LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
   """"RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
   """"RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1"""",
   """"cid":"({cid}[^"]+)""",
   """"event_platform":\s*"({os}[^"]+)"""
   """"ContextBaseFileName":"({file_name}[^"]+)""""
   """"ComputerName":"({host}[\w\-\.]+)""""
   """exa_json_path=$.OciContainerId,exa_field_name=container_id""",
   """exa_json_path=$.hostname,exa_field_name=host""",
   """exa_json_path=$.timestamp,exa_field_name=time""",
   """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
   """exa_json_path=$.aid,exa_field_name=aid""",
   """exa_json_path=$.name,exa_field_name=event_name""",
   """exa_regex="LocalAddressIP(4|6)":"(0:0:0:0:0:0:0:0|0.0.0.0|127.0.0.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_regex="RemoteAddressIP(4|6)":"(0:0:0:0:0:0:0:0|0.0.0.0|127.0.0.1|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """exa_json_path=$.LocalPort,exa_field_name=src_port""",
    """exa_json_path=$.RemotePort,exa_field_name=dest_port""",
    """exa_json_path=$.ConnectionDirection,exa_regex=({direction}(0|1))""",
    """exa_json_path=$.Protocol,exa_field_name=protocol""",
    """exa_json_path=$.src-account-name,exa_field_name=account_name""",
    """exa_json_path=$.ContextProcessId,exa_field_name=process_guid""",
    """exa_json_path=$.aip,exa_field_name=aip""",
    """exa_regex=ConnectionDirection":"({direction}1)",.+?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","LocalPort":"*({dest_port}\d+)"*,.+?"RemoteAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*"*({=src_port}\d+)"""",
    """exa_regex=ConnectionDirection":"({direction}0)",.+?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","LocalPort":"*({src_port}\d+)"*,.+?"RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*"*({=dest_port}\d+)"""",
    """exa_regex="LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
   """exa_regex="LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
   """exa_regex="RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
   """exa_regex="RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1"""",
   """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.event_platform,exa_field_name=os"""
   """exa_json_path=$.ContextBaseFileName,exa_field_name=file_name"""
   """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
  ]


}
```