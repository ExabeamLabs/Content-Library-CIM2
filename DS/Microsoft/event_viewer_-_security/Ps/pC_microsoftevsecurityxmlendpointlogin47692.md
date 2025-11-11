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
  """Account Name(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[\w._\-]+))?[\s;]*Account Domain(:|=)"""
  """Service Name(:|=)\s*({dest_host}[\w\-\.]+)\$[\s;]*Service ID"""
  """Service Name(:|=)\s*({service_name}[^\s;]+)[\s;]*Service ID"""
  """Client Address(:|=)\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """Failure Code(:|=)((?-i)\\+[rnt])*\s*({failure_code}({result_code}[^\s:;\\]+))((?-i)\\+[rnt])*\s*[\s;]*[\w\s]+(:|=)"""
  """Ticket Options(:|=)\s*({ticket_options}[^\s;:]+)[\s;]*[\w\s]+(:|=)"""
  """Ticket Encryption Type(:|=)\s*({ticket_encryption_type}[^\s:;]+)[\s;]*[\w\s]+(:|=)"""
  """<Level>({run_level}[^<]+)<"""
  ]
  ParserVersion = "v1.0.0"


}
```