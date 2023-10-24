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
    """"LocalAddressIP4":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"LocalPort":"({src_port}\d+)""",
    """"RemoteAddressIP4":"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """"RemotePort":"({dest_port}\d+)""",
    """"ConnectionDirection":"({direction}[^"]+)""",
    """"ContextProcessId":"({process_guid}[^"]+)""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """"name":"({process_name}[^"]+)""",
    """"LocalAddressIP6":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"RemoteAddressIP6":"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """src-account-name":"({account_name}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"Size":"({bytes}\d+)"""",
    """"Protocol":"({protocol}[^"]+)""",
    """ConnectionDirection":"({direction}1)",.+?"LocalAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","LocalPort":"*({dest_port}\d+)"*,.+?"RemoteAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?","RemotePort":\s*"*({=src_port}\d+)"""",
    """ConnectionDirection":"({direction}0)",.+?"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","LocalPort":"*({src_port}\d+)"*,.+?"RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?","RemotePort":\s*"*({=dest_port}\d+)"""",
   """"LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
   """"LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
   """"RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
   """"RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1"""",
   """"cid":"({cid}[^"]+)"""
    
 ]


}
```