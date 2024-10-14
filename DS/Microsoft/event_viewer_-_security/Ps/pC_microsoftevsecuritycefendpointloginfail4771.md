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
    """\sdvchost=({host}[\w\-.]+)"""
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
    """\sdntdom=({user_sid}[^\s\\]+)"""
    """\scs4=({result_code}[^\s]+)"""
    """destinationServiceName =\s*\w+\/(?=\w)({domain}.+?)\s+\w+="""
    """\scs3=(?:::[\w]+:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """"\sdst=(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+\w+="""
    """\sreason=({failure_reason}[^=]+?)\s+\w+="""
    """\ssourceGeoLocationInfo=({location}[^=]+?)\s+\w+="""
  ]
  DupFields = [
    "result_code->failure_code"
  ]


}
```