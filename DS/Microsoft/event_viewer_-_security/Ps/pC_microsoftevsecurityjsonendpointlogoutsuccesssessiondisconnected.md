#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-logout-success-sessiondisconnected"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """McAfee_SIEM:""", """A session was disconnected from a Window Station.""" ]
  Fields = [
  """({event_name}A session was disconnected from a Window Station)"""
  """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"id":\d*({event_code}4779)"""
  """"firsttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
  """"DomainID":"({domain}[^"]+)"""
  """"HostID":"({host}[^"]+)"""
  """"UserIDSrc":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"Source_Logon_ID":"({login_id}[^"]+)"""
  ]
ParserVersion = "v1.0.0"


}
```