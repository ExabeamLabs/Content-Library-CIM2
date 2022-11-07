#### Parser Content
```Java
{
Name = cyberark-vault-mix-app-login-success-logon
  ParserVersion = v1.0.0
  Vendor = CyberArk
  Product = Vault
  TimeFormat = "epoch"
  Conditions = [  """|Cyber-Ark|Vault|""", """Action=Logon""" ]
  Fields = [
    """(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({host}[\w\-.]+) (LEEF|CEF)""",
    """(LEEF|CEF):([^\|]*?\|){4}({event_code}\d+)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """usrName =(({domain}[^\\=]+)(\\)+)?(({email_address}[^@]+@[^.]+\.[^=]+?)|({user}[^=]+?))\s+(\w+=|$)""",
    """\ssrc=({src_ip}[A-Fa-f\d:.]+)""",
    """\sEventMessage=(\s+|({event_subtype}[^=]+?))\s+(\w+=|$)""",
    """\sSafe=(\s+|({safe_value}[^=]+?))\s+(\w+=|$)""",
    """\sGatewayStation=({gateway_station}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\sReason=(\s+|({reason}[^=]+?))\s+(\w+=|$)""",
    """({app}Cyber-Ark)""",
    """Action=({action}[^=]+?)\s*\w+="""
  ]
  DupFields=[ "host->dest_host" ]


}
```