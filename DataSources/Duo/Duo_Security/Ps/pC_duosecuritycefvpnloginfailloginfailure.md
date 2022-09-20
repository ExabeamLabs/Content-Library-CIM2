#### Parser Content
```Java
{
Name = duo-security-cef-vpn-login-fail-loginfailure
  ParserVersion = v1.0.0
  Vendor = Duo
  Product = Duo Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
"""destinationServiceName =DUO"""
"""VPN"""
"""FAILURE"""
"""new_enrollment"""
]
  Fields = [
    """"isotimestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)"""",
    """\WdestinationServiceName =(|({app}.+?))(\s+\w+=|\s*$)""",
    """"factor"+:\s*"+({operation}[^"]+)"""",
    """"username":"(?!AD Sync:)({user}[^"]+)""",
    """"device":\s*"({object}[^"]+)""",
    """"type":\s*"({alert_type}[^"]+)""",
    """"error":\s*"({failure_reason}[^"]+)""",
    """email?:\s+({email_address}[^"]+)]""",
    """ip(_address)?":\s*"({src_ip}[A-Fa-f:\d.]+)""",
    """"result":\s*"({result}[^"]+)""",
    """"browser":\s*({browser}[^"]+)""",
    """"os":\s*({os}[^"]+)""",
    """"city":\s*"({location_city}[^"]+)""",
    """"state":\s*"({location_state}[^"]+)""",
    """"country":\s*"({location_country}[^"]+)""",
    """"integration":\s*"({service_name}[^"]+)""""
  ]


}
```