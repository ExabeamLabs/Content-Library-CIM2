#### Parser Content
```Java
{
Name = delinea-centrifyztps-sk4-app-login-centrify
  Vendor = Delinea
  Product = Centrify Zero Trust Privilege Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""destinationServiceName =Centrify""", """Centrify""", """"EventType":"""" ]
  Fields = [
    """"NormalizedUser":"(({email_address}[^@"]+@({email_domain}[^\."]+\.[^"]+))(?<!local)|(({user}[^"@]+)(@({domain}[^"]+)?)))"""",
    """"EventType":"({operation}[^"]+)"""
    """destinationServiceName =({app}[^\s]+)""",
    """"CredentialType":"({object}[^"]+)""",
    """"AuthoritySource":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"ComputerName":"({dest_host}[^"]+)""",
    """"EventMessage":"({additional_info}[^"]+)""",
    """"FailReason":"({failure_reason}[^"]+)""",
    """"AuthMethod":"(?:None|({auth_method}[^"]+))""",
    """"RequestUserAgent":"({user_agent}[^"]+)""",
    """"FromIPAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"RequestUserAgent":"(?:-|Mozilla\/[^=]+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin))""",
    """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """cat=({event_name}[^\s]+)""",
  ]
  ParserVersion = v1.0.0


}
```