#### Parser Content
```Java
{
Name = "checkpoint-sg-kv-vpn-login-success-login"
  Vendor = "Check Point"
  Product = "Check Point Security Gateway"
  TimeFormat = "epoch_sec"
  Conditions = [ """"MAB Login Activity"""", """product""", """"Connectra"""", """action""", """:"Log In"""" ]
  Fields = [
    """(\"\s|,)"?time"?:"?({time}\d{10})""",
    """action"?:"({action}[^",;]+)""",
    """origin"?:"({origin_ip}[A-Fa-f:\d.]+)""",
    """origin_?sic_?name"?:"CN=({origin_name}[^",]+)""",
    """src"?:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """user"?:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)"""
    """event_name"?:"({event_name}[^"]+)""",
    """cu_rule_id"?:"({rule_id}[^"]+)""",
    """cvpn_category"?:"({category}[^"]+)""",
    """device_identification"?:"({device_id}[^"]+)""",
    """cu_rule_category"?:"({rule_type}[^"]+)""",
    """hostname"?:"({host}[\w\-\.]+)""",
    """severity"?:"?({severity}[^",]+)""",
    """auth_method"?:"({auth_method}[^"]+)""",
    """client_name"?:"({client_name}[^"]+)""",
    """host_type"?:"({host_type}[^"]+)""",
    """tunnel_protocol"?:"({tunnel_protocol}[^"]+)""",
    """proto"?:"?({protocol}[^",]+)""",
    """status"?:"({result}[^"]+)""",
    """os_name"?:"({os_type}[^"]+)""",
    """os_version"?:"?({os_version}[^",]+)"""
    """service"?:"?({dest_port}\d+)"""
]
  ParserVersion = "v1.0.0"


}
```