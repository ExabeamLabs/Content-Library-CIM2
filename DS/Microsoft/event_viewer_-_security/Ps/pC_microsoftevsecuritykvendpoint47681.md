#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-4768-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """__li_source_path="""
  """A Kerberos authentication ticket (TGT) was requested"""
  """eventid="4768""""
]
Fields = [
  """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
  """\W__li_source_path=\"({host}[\w\.-]+)\""""
  """({event_code}4768)"""
  """Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@([^\s]+))?\s+Supplied Realm Name"""
  """Client Address:\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Result Code:\s+({result_code}[\w]+)"""
  """Supplied Realm Name:\s+({domain}[^\s]+)"""
  """User ID:\s+(?:NULL SID|({user_sid}.+?))\s+Service Information"""
  """Service Name:\s*(\\+r|\\+t|\\+n)*(({service_name}[^=:\\_]+?)(_[^"\<]+?)?)\s*(\\+r|\\+t|\\+n)*Service """
  """Ticket Options:\s*({ticket_options}[^\s]+)"""
  """Ticket Encryption Type:\s*({ticket_encryption_type}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```