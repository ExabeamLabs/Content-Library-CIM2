#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-success-4770"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4770|"""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was renewed)"""
    """\sexternalId=({event_code}\d+)"""
    """\srt=({time}\d{13})"""
    """\sdntdom=({domain}[^\s]+)"""
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^\s]+)?\s+\w+="""
    """\sdvc=({host}[a-fA-F:\d.]+)"""
    """\s(dvchost|dhost)=({dest_host}({host}[\w\-.]+))"""
    """\scs3=(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sdst=(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+\w+="""
    """\sdestinationServiceName =({service_name}\S+)"""
    """\sdestinationServiceName =({dest_host}\S+\$)"""
    """ncryption_,Type=({ticket_encryption_type}[^\s]+)"""
    """Ticket_,Options=({ticket_options}[^\s]+)"""
    """\ssourceGeoLocationInfo=({location}[^=]+?)\s+\w+="""
  ]


}
```