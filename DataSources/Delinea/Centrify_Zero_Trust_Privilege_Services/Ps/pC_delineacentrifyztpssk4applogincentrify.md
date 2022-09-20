#### Parser Content
```Java
{
Name = delinea-centrifyztps-sk4-app-login-centrify
  Vendor = Delinea
  Product = Centrify Zero Trust Privilege Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""destinationServiceName =Centrify""", """Centrify""", """"EventType":"""" ]
  Fields = [
    """"NormalizedUser":"(({email_address}[^@"]+@({email_domain}[^\."]+\.[^"]+)")|(({user}[^"@]+)(@({domain}[^"]+)?)))""",
    """"EventType":"({operation}[^"]+)"""
    """destinationServiceName =({app}[^\s]+)""",
    """"CredentialType":"({object}[^"]+)""",
    """"AuthoritySource":"({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """"ComputerName":"({dest_host}[^"]+)""",
    """"EventMessage":"({additional_info}[^"]+)""",
    """"FailReason":"({failure_reason}[^"]+)""",
    """"AuthMethod":"(?:None|({auth_method}[^"]+))""",
    """"RequestUserAgent":"({user_agent}[^"]+)""",
    """"FromIPAddress":"({src_ip}[A-Fa-f\d:.]+)""",
    """"RequestUserAgent":"(?:-|Mozilla\/[^=]+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin))""",
    """src=({src_ip}[A-Fa-f\d:.]+)""",
    """cat=({event_name}[^\s]+)""",
  ]
  ParserVersion = v1.0.0


}
```