#### Parser Content
```Java
{
Name = "microsoft-evterminalservicesgateway-str-rdp-traffic-success-connectedtoresource"
Vendor = "Microsoft"
Product = "Event Viewer - TerminalServices-Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Microsoft-Windows-TerminalServices-Gateway"""
  """connected to resource"""
]
Fields = [
  """on client computer "+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """connected to resource "+(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^"]+))""",
  """The user "+({domain}[^\\]+)?(\\)?({user}[^"]+)""",
  """Connection protocol used: "+({protocol}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```