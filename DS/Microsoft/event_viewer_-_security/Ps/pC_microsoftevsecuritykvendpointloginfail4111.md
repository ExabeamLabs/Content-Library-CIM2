#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-411-1
  ParserVersion = "v1.0.0"
  Conditions = [ """Message=Token validation failed""", """EventIDCode=411""" ]
  Fields = ${MicrosoftParserTemplates.q-adfs-auth.Fields}[
    """\sComputer=({host}.+?)(\s+\w+=|\s*$)""",
    """Token Type:\s*({auth_method}.+?)\s*Client IP:""",
    """Exception details:\s*({additional_info}.{1,250})""",
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Error message:""",
    """Error message:\s*({failure_reason}.+?)\s*Exception details:""",
    """\sUser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)""",
  ]

q-adfs-auth = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch_sec"
  Fields = [
    """\sTimeGenerated=({time}\d{10})""",
    """\sEventIDCode=({event_code}\d+)""",
    """\sUser=({account}.+?)(\s+\w+=|\s*$)""",
    """\sDomain=({account_domain}.+?)(\s+\w+=|\s*$)""",
    """\sMessage=({event_name}[^=\.]+)""",
    """<IpAddress>({additional_info}[^<]+)</IpAddress>""",
    """<IpAddress>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</IpAddress>""",
    """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</IpAddress>""",
    """<ClaimsProvider>(?:N\/A|({domain}[^<]+))</ClaimsProvider>""",
    """<UserId>(({domain}[^<\\]+)\\+)?(N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</UserId>""",
    """<FailureType>(?:None|({failure_reason}[^<]+))</FailureType>""",
    """<Server>({auth_server}[^<]+)</Server>""",
    """:({service_name}[^:>]+)</RelyingParty>""",
    """<PrimaryAuth>(N\/A|[^<]+?\/({auth_method}[^<\/]+))</PrimaryAuth>""",
  
}
```