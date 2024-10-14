#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-authentication-success-4768"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4768"""
  ]
  Fields = [
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
    """({event_code}4768)"""
    """\srt=({time}\d{13})"""
    """\sduser=\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """\scs3=(::[\w]+:)?({src_ip}((([0-9a-fA-F.:]{1,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\scs4=({result_code}\w+)"""
    """\sdvchost=({host}[\w\-.]+)"""
    """\sdntdom=({domain}[^\s]+)"""
    """Service_,ID=({user_sid}[^\s]+)\s"""
    """\sdestinationServiceName =({service_name}\S+)"""
    """ncryption_,Type=({ticket_encryption_type}[^\s]+)"""
    """Ticket_,Options=({ticket_options}[^\s]+)"""
    """\ssourceGeoLocationInfo=({location}[^=]+?)\s+\w+="""
  ]


}
```