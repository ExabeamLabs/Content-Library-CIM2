#### Parser Content
```Java
{
Name = cisco-duo-cef-vpn-login-fail-loginfailure
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "epoch_sec"
  Conditions = [
"""destinationServiceName =DUO"""
"""VPN"""
"""FAILURE"""
"""new_enrollment"""
]
  Fields = [
    """"isotimestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)"""",
    """\"timestamp\":\s*({time}\d{10})""",
    """\WdestinationServiceName =(|({app}.+?))(\s+\w+=|\s*$)""",
    """"factor"+:\s*"+({operation}[^"]+)"""",
    """"username":"(?!AD Sync:)({user}[^"]+)""",
    """"device":\s*"({object}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"error":\s*"({failure_reason}[^"]+)""",
    """email?:\s+({email_address}[^"]+)]""",
    """ip(_address)?":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"result":\s*"({result}[^"]+)""",
    """"browser":\s*({browser}[^"]+)""",
    """"os":\s*({os}[^"]+)""",
    """"city":\s*"({city}[^"]+)""",
    """"state":\s*"({state}[^"]+)""",
    """"country":\s*"({country}[^"]+)""",
    """"integration":\s*"({service_name}[^"]+)""""
  ]
DupFields = [
"operation->factor"
]


}
```