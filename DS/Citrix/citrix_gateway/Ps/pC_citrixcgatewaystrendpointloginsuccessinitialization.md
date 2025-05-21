#### Parser Content
```Java
{
Name = "citrix-cgateway-str-endpoint-login-success-initialization"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "MM/dd/yyyy:HH:mm:ss Z"
Conditions = [
  """ After Initialization """
]
Fields = [
   """\Wrt=({time}\d{13})""",
   """\Wdvchost=({host}[\w\-.]+)\s+\w+=""",
   """user\s*(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*clientip\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_category}SSLVPN Message)?\s.*?user\s*(({domain}[^\\\s]+)\\+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*clientip\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(request:\s*({action}[^\s]+))?"""
   """SSO\s+({event_name}[^:]+): After Initialization user (({domain}[^\\\s]+)\\+)?(-|({email_address}[^@"\s]+@[^@"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+clientip\s+(127.0.0.1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s"""
  """({event_name}ns_sslvpn_process_sso_conn)"""
]
ParserVersion = "v1.0.0"


}
```