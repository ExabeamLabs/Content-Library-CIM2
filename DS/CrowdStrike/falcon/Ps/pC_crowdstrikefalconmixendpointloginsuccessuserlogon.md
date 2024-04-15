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
"""\"aip\":\"({aip}[^\"]+)""",
"""suser=((?i)system|({user}[^\s]+))""",
"""suid=({user_sid}[^\s]+)""",
"""\"AuthenticationPackage\":\"({auth_package}[^\"]+)""",
"""timestamp":\s*"({time}\d{10})""",
"""\"LogonType\":\"({login_type}\d+)""",
""""UserPrincipal":"({user}[^@"]+)@({domain}[^"]+)""",
"""UserName":"((?i)system|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+))((?i)(?<!local)(?<!loc))|({=user}[^@<;]+?)(?:@({=domain}[^<.]+)[^"]*)?)"""",
"""\"LogonServer\":\"({auth_server}[^\"]+)""",
"""\"ClientComputerName\\?\"+:\\?\"+(-|({dest_host}[^\"\\,]+))""",
"""\"UserSid\":\"({user_sid}[^\"]+)""",
"""\"aid\":\"({aid}[^\"]+)""",
"""\"event_simpleName\":\"({event_code}[^\"]+)""",
"""\"LogonDomain\":\"(NT AUTHORITY|({domain}[^\"]+))""",
""""event_platform\\*":\\*"({os}[^"\\]+)"""

  ]
  DupFields = [ "user->account" ]


}
```