#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-network-session-success-listenip
  ParserVersion = v1.0.0
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  Conditions = [ 
""""event_simpleName":""""
"""NetworkListenIP""" 
]
  Fields = [
    """"timestamp":\s*"*({time}\d{13})"""",
    """"LocalAddressIP4":"(0.0.0.0|0:0:0:0:0:0:0:0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"LocalPort":"({src_port}\d+)""",
    """"RemoteAddressIP4":"(0.0.0.0|0:0:0:0:0:0:0:0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"RemotePort":"({dest_port}\d+)""",
    """"ConnectionDirection":"({direction}[^"]+)""",
    """"ContextProcessId":"({process_guid}[^"]+)""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """"name":"({process_name}[^"]+)""",
    """"LocalAddressIP6":"(0.0.0.0|0:0:0:0:0:0:0:0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"RemoteAddressIP6":"(0.0.0.0|0:0:0:0:0:0:0:0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"aid":"({aid}[^"]+)"""
 ]


}
```