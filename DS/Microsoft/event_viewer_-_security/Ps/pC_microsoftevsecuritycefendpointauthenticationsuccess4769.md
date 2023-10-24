#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-authentication-success-4769"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4769"""
  ]
  Fields = [
    """({event_name}A Kerberos service ticket was requested)"""
    """({event_code}4769)"""
    """\srt=({time}\d{13})"""
    """\sduser=({user}[\w\.\-]{1,40}\$?)(@({domain}.+?))?\s+\w+="""
    """\sdestinationServiceName =({dest_host}\S+\$)\s"""
    """\sdestinationServiceName =({service_name}\S+)"""
    """\scs3=(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\scs4=({result_code}[^\s]+)"""
    """\sdvchost=({host}[^\s]+)"""
    """ncryption_,Type=({ticket_encryption_type}[^\s]+)"""
    """Ticket_,Options=({ticket_options}[^\s]+)"""
  ]


}
```