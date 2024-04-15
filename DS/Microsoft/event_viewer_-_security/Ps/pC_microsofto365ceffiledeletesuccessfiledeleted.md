#### Parser Content
```Java
{
Name = "microsoft-o365-cef-file-delete-success-filedeleted"
Conditions = [
  """|Microsoft|"""
  """|FileDeleted|"""
  """eventId="""
]
ParserVersion = "v1.0.0"

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
    """<IpAddress>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</IpAddress>""",
    """({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</IpAddress>""",
    """<ClaimsProvider>(?:N\/A|({domain}[^<]+))</ClaimsProvider>""",
    """<UserId>(({domain}[^<\\]+)\\+)?({user}(?!N\/A)[^<\\]+)</UserId>""",
    """<FailureType>(?:None|({failure_reason}[^<]+))</FailureType>""",
    """<Server>({auth_server}[^<]+)</Server>""",
    """:({service_name}[^:>]+)</RelyingParty>""",
    """<PrimaryAuth>(N\/A|[^<]+?\/({auth_method}[^<\/]+))</PrimaryAuth>""",
  
}
```