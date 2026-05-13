#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4769-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Conditions = [
  """<EventID>4769</EventID>"""
  """A Kerberos service ticket was requested"""
  """Account Name"""
  """Microsoft-Windows-Security-Auditing"""
  ]
  Fields = [
  """({event_name}A Kerberos service ticket was requested)"""
  """TimeCreated SystemTime=('|")?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """TimeCreated SystemTime=('|")?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)"""
  """Computer>({host}[\w\-.]+)<\/Computer"""
  """({event_code}4769)"""
  """Account Name(:|=)\s*(\\r|\\n|\\t)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?(\\r|\\n|\\t)*[\s;]*Account Domain(:|=)"""
  """Service Name(:|=)\s*(\\r|\\n|\\t)*({dest_host}[\w\-\.]+)\$(\\r|\\n|\\t)*[\s;]*Service ID"""
  """Service Name(:|=)\s*(\\r|\\n|\\t)*({service_name}[^\s;]+?)(\\r|\\n|\\t)*[\s;]*Service ID"""
  """Client Address(:|=)\s*(\\r|\\n|\\t)*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[^\s:;\\]+))(\\r|\\n|\\t)*[\s;]*[\w\s]+(:|=)"""
  """Ticket Options(:|=)\s*(\\r|\\n|\\t)*({ticket_options}[^\s\\;]+?)[\s;]*(\\r|\\n|\\t)*Ticket Encryption Type(:|=)"""
  """Ticket Encryption Type(:|=)\s*(\\r|\\n|\\t)*({ticket_encryption_type}[^\s\\;]+?)(\\r|\\n\\t)*[\s;]*Failure Code(:|=)"""
  """<Level>({run_level}[^<]+)<"""
  """<Channel>({channel}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```