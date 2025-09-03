#### Parser Content
```Java
{
Name = "microsoft-nps-xml-endpoint-authentication-success-6272"
Vendor = "Microsoft"
Product = "Microsoft Network Policy Server"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>6272</EventID>"""
  """<Message>Network Policy Server granted access to a user"""
]
Fields = [
  """SystemTime=('|")({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>({host}[\w\-.]+)"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """({event_code}6272)"""
  """('|")SubjectUserName('|")>(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """('|")SubjectDomainName('|")>(?:-|({domain}[^\s\<]+))"""
  """('|")SubjectUserName('|")>(?:({user_type}host)/)?(({src_domain}[^\\]+)\\+)?({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """('|")SubjectDomainName('|")>(?:-|({src_domain}[^\s\<]+))"""  
  """('|")FullyQualifiedSubjectUserName('|")>(({domain}[^\\]+)\\+)?(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """('|")NASIdentifier('|")>(?:-|({location}[\w\-.]+))"""
  """('|")CallingStationID('|")>(?:-|({src_mac}[^\<]+))"""
  """('|")AuthenticationProvider('|")>(?:-|({auth_server}[^\<]+))"""
  """('|")FullyQualifiedSubjectMachineName('|")>(?:-|({user_type}.+?))(\/[^\/\s]+)?<"""
  """('|")NASIPv6Address('|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """('|")NASIPv4Address('|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """('|")EAPType('|")>(?:-|({auth_type}[^\<]+))"""
  """('|")QuarantineState('|")>(?:-|({access_type}[^\<]+))"""
  """<Level>({run_level}[^<]+)<"""
]
ParserVersion = "v1.0.0"


}
```