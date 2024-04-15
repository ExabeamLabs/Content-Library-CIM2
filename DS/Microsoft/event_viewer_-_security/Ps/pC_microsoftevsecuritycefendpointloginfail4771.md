#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-fail-4771"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4771|"""
  ]
  Fields = [
    """({event_name}Kerberos pre-authentication failed)"""
    """\sexternalId=({event_code}\d+)"""
    """\srt=({time}\d{13})"""
    """\sdvc=({host}[a-fA-F:\d.]+)"""
    """\sdvchost=({host}[^\s]+)"""
    """\sduser=({user}.+?)\s+\w+="""
    """\sdntdom=({user_sid}[^\s\\]+)"""
    """\scs4=({result_code}[^\s]+)"""
    """destinationServiceName =\s*\w+\/(?=\w)({domain}.+?)\s+\w+="""
    """\scs3=(?:::[\w]+:|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  ]
  DupFields = [
    "host->dest_host"
    "result_code->failure_code"
  ]


}
```