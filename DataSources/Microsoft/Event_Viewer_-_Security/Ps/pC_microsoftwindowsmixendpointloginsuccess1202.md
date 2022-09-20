#### Parser Content
```Java
{
Name = microsoft-windows-mix-endpoint-login-success-1202
  ParserVersion = "v1.0.0"
  Conditions = [ """Message=The Federation Service validated a new credential""", """EventIDCode=1202""" ]

q-adfs-auth = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Fields = [
    """\sTimeGenerated=({time}\d{10})""",
    """\sEventIDCode=({event_code}\d+)""",
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)""",
    """\sUser=({account}.+?)(\s+\w+=|\s*$)""",
    """\sDomain=({account_domain}.+?)(\s+\w+=|\s*$)""",
    """\sMessage=({event_name}[^=\.]+)""",
    """<IpAddress>({additional_info}[^<]+)</IpAddress>""",
    """<IpAddress>({src_ip}[a-fA-F\d.:]+)</IpAddress>""",
    """({src_ip}[a-fA-F\d.:]+)</IpAddress>""",
    """<ClaimsProvider>(?:N\/A|({domain}[^<]+))</ClaimsProvider>""",
    """<UserId>(({domain}[^<\\]+)\\+)?({user}(?!N\/A)[^<\\]+)</UserId>""",
    """<FailureType>(?:None|({failure_reason}[^<]+))</FailureType>""",
    """<Server>({auth_server}[^<]+)</Server>""",
    """:({service_name}[^:>]+)</RelyingParty>""",
    """<PrimaryAuth>(N\/A|[^<]+?\/({auth_method}[^<\/]+))</PrimaryAuth>""",
  
}
```