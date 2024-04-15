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
    """\sduser=({user}[^@]+)(@[^\s]+)?\s+\w+="""
    """\sdvc=({host}[a-fA-F:\d.]+)"""
    """\sdvchost=({host}[^\s]+)"""
    """\scs3=(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\sdestinationServiceName =({service_name}\S+)"""
    """\sdestinationServiceName =({dest_host}\S+\$)"""
    """ncryption_,Type=({ticket_encryption_type}[^\s]+)"""
    """Ticket_,Options=({ticket_options}[^\s]+)"""
  ]


}
```