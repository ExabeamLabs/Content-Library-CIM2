#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-endpoint-login-success-useridentity"
  ParserVersion = "v1.0.0"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  TimeFormat = "epoch_sec"
  Conditions = [ 
"""event_simpleName":"""
""""UserIdentity""""
""""aid"""" 
]
  Fields = [
"""\"timestamp\":\s*\"({time}\d{10})"""
"""\"UserPrincipal\":\s*\"(?:[^\"@]+@)?({domain}[^\"]+)"""
"""\"aid\":\s*\"({aid}[^\"]+)"""
"""\"event_simpleName\":\s*\"({event_code}[^\"]+)"""
"""\"LogonType\":\s*\"({login_type}\d+)"""
"""\"UserName\":\s*\"(({full_name}({first_name}[^\s\"]+)\s({last_name}[^\"]+))|({user}[^\"\s]+))"""
"""\"+AuthenticationPackage\"+:\s*\"+({auth_package}[^\"]+)\"+,"""
"""\"+event_platform\"+:\s*\"+({event_platform}[^\"]+)\"+"""
  ]


}
```