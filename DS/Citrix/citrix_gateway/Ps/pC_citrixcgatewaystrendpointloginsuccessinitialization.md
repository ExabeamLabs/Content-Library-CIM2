#### Parser Content
```Java
{
Name = "citrix-cgateway-str-endpoint-login-success-initialization"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "MM/dd/yyyy:HH:mm:ss"
Conditions = [
  """ After Initialization """
]
Fields = [
   """({time}\d\d\/\d\d\/\d\d\d\d:\d\d:\d\d:\d\d \w+)\s+({host}[\w.\-]+)(\s+\S+){3}\s+({event_category}SSLVPN Message)?\s.*?user\s*(({domain}[^\\\s]+)\\+)?({user}[^\s]+)\s*clientip\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(request:\s*({action}[^\s]+))?"""
   """SSO\s+({event_name}[^:]+): After Initialization user (({domain}[^\\\s]+)\\+)?({user}.+?)\s+clientip\s+(127.0.0.1|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s"""
  """({event_name}ns_sslvpn_process_sso_conn)"""
]
ParserVersion = "v1.0.0"


}
```