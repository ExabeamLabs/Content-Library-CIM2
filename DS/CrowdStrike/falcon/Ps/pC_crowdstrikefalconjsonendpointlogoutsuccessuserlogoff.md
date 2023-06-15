#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-endpoint-logout-success-userlogoff
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """"event_simpleName":"UserLogoff"""", """"destinationServiceName":"CrowdStrike"""" ]
  Fields = [
    """timestamp":"({time}\d{13})"""
    """"event_simpleName":"({event_name}[^"]+)"""",
    """"UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({linked_service_account}OVService[^"]+)|({user_sid}S-[^"]+)|({user}[\w\-\.]+\$?))""""
    """"LogonType":"({login_type}\d+)"""
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"LogonDomain":"({domain}[^"]+)"""",
    """"AuthenticationPackage":"({auth_package}[^"]+)"""",
    """"UserSid":"({user_sid}[^"]+)""",
    """"UserPrincipal":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)(?<!localdomain)"""",
    """"event_platform":"({os}[^"]+)"""",
  ]


}
```