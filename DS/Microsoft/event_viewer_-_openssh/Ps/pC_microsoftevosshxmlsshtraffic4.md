#### Parser Content
```Java
{
Name = "microsoft-evossh-xml-ssh-traffic-4"
Vendor = "Microsoft"
Product = "Event Viewer - OpenSSH"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<EventID>4<"""
""">sshd<"""
"""<Channel>OpenSSH/Operational<"""
]
Fields = [
  """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)('|")\/>"""
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>"""
  """<Keywords>({result}[^<]+)"""
  """<EventID>({event_code}[^<]+)"""
  """<Level>({run_level}[^<]+)<"""
  """<Security UserID=('|")({user_sid}[^'"]+)('|")\/>"""
  """<Data Name =('|")payload('|")>({additional_info}[^<]+)"""
  """<Data Name =('|")process('|")>({operation}[^<]+)"""
  """for ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) port ({src_port}\d+)"""
  """from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) port ({src_port}\d+)"""
]
ParserVersion = "v1.0.0"


}
```