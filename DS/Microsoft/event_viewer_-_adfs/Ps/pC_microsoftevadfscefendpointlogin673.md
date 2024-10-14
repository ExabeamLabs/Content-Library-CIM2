#### Parser Content
```Java
{
Name = "microsoft-evadfs-cef-endpoint-login-673"
Vendor = "Microsoft"
Product = "Event Viewer - ADFS"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """|Security:673|"""
]
Fields = [
  """({event_name}Account Logon)"""
  """({event_code}673)"""
  """\srt=({time}\d{13})"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@(.+?))?\s+\w+="""
  """\ssuser=.+?(@({domain}.+?))?\s+\w+="""
  """\sdestinationServiceName =({dest_host}\S+\$)\s"""
  """\sdestinationServiceName =({service_name}\S+)"""
  """\scs4=({result_code}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """Ticket_,Options=({ticket_options}[^\s]+)"""
  """Ticket_,Encryption_,Type=({ticket_encryption_type}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```