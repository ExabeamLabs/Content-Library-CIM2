#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-endpoint-login-success-hostinfo"
  ParserVersion = "v1.0.0"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ExtractionType = json
  TimeFormat = "epoch"
  Conditions = [ 
""""event_simpleName":"HostInfo""""
""""aid"""" 
]
  Fields = [      
    """"timestamp":\s*"*({time}\d{13})"""",
    """"+MachineDn"+:"+CN\\*(=|u003d)?({dest_host}[^,]+)""",
    """"aid":"({aid}[^"]+)""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """suser=(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"MachineDomain":"({domain}[^"]+)"""",
    """"aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"SiteName":"({location}[^"]+)"""",
    """"cid":"({cid}[^"]+)""",
    """"event_platform":"({os}[^"]+)"""",
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"ComputerName":"({host}[\w\-\.]+)"""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_regex="timestamp":\s*"*({time}\d{13})""""
	  """exa_json_path=$.MachineDn,exa_regex=CN\\*(=|u003d)?({dest_host}[^,]+)""",
	  """exa_json_path=$.aid,exa_field_name=aid""",
	  """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
	  """exa_json_path=$.MachineDomain,exa_field_name=domain""",
	  """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	  """exa_json_path=$.SiteName,exa_field_name=location""",
	  """exa_json_path=$.cid,exa_field_name=cid""",
	  """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
  ]
  DupFields = [ "dest_host->host" ]


}
```