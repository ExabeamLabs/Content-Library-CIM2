#### Parser Content
```Java
{
Name = cyberark-pam-mix-app-login-success-logon
  ParserVersion = v1.0.0
  Vendor = CyberArk
  Product = "CyberArk Privilege Access Manager"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [  """|Cyber-Ark|Vault|""", """Action=Logon""" ]
  Fields = [
    """(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({host}[\w\-.]+) (LEEF|CEF)""",
    """(LEEF|CEF):([^\|]*?\|){4}({event_code}\d+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """usrName =(({domain}[^\\=]+)(\\)+)?(({email_address}[^@"\.]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s+\w+=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sEventMessage=(\s+|({event_subtype}[^=]+?))\s+(\w+=|$)""",
    """\sSafe=(\s+|({safe_value}[^=]+?))\s+(\w+=|$)""",
    """\sGatewayStation=({gateway_station}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sReason=(\s+|({result_reason}[^=]+?))\s+(\w+=|$)""",
    """({app}Cyber-Ark)""",
    """Action=({action}[^=]+?)\s*\w+="""
  ]
  DupFields=[ "host->dest_host" ]


}
```