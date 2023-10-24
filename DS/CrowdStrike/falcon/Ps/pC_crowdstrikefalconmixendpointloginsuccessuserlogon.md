#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-endpoint-login-success-userlogon"
  ParserVersion = "v1.0.0"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""event_simpleName":"UserLogon""""
""""aid"""" 
]
  Fields = [
""""aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""suser=((?i)system|({user}[\w\.\-]{1,40}\$?))""",
"""suid=({user_sid}[^\s]+)""",
""""AuthenticationPackage":"({auth_package}[^\"]+)""",
"""timestamp":\s*"({time}\d{10})""",
""""LogonType":"({login_type}\d+)""",
""""UserPrincipal":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!LOCAL)(?<!local)(?<!loc)(?<!prd)(?<!localdomain)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^,"]+)[^"]*)?)"""",
"""UserName":"((?i)system|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+))(?i))(?<!local)(?<!loc)|((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^"]+)[^"]*)?))"""",
""""UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!local)(?<!loc)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^"]+)[^"]*)?)""""
""""LogonServer":"({auth_server}[^\"]+)""",
""""ClientComputerName"+:"+(-|({dest_host}[^\"\\,]+))""",
""""UserSid":"({user_sid}[^\"]+)""",
""""aid":"({aid}[^\"]+)""",
""""event_simpleName":"({event_code}[^\"]+)""",
""""LogonDomain":"(NT AUTHORITY|({domain}[^\"]+))""",
""""RemoteAddressIP4":"({dest_ip}[A-Fa-f:\d\.]+)"""",
""""event_platform":"({os}[^"\\]+)"""
""""aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""cid":"({cid}[^"]+)"""
  ]
  DupFields = [ "user->account", "aip->src_ip" ]


}
```