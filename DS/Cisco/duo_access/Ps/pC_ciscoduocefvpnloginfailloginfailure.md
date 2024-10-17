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
"""new_enrollment"""
]
  Fields = [
    """"isotimestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)"""",
    """\"timestamp\":\s*({time}\d{10})""",
    """\WdestinationServiceName =(|({app}.+?))(\s+\w+=|\s*$)""",
    """"factor"+:\s*"+({factor}[^"]+)"""",
    """"username":"(?!AD Sync:)({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """"device":\s*"({object}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"error":\s*"({failure_reason}[^"]+)""",
    """email?:\s+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))]""",
    """ip(_address)?":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"result":\s*"({result}[^"]+)""",
    """"browser":\s*(null|({browser}[^"]+))""",
    """"os":\s*(null|({os}[^"]+))""",
    """"city":\s*"({city}[^"]+)""",
    """"state":\s*"({state}[^"]+)""",
    """"country":\s*"({country}[^"]+)""",
    """"integration":\s*"({service_name}[^"]+)"""",
    """""reason":"({failure_reason}[^"]+)""""
  ]


}
```