#### Parser Content
```Java
{
Name = "juniper-ps-str-vpn-login-success-connected-2"
Vendor = "Ivanti"
Product = "Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Juniper: """
  """ - Connected to"""
]
Fields = [
  """(Juniper:|PulseSecure:)\s+\S+\s+\S+\s+-\s+({host}[\w\.\-]+)\s+-"""
  """(Juniper:|PulseSecure:)\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\s+-\s+\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]"""
  """\s+-\s+\[[^\]]+\]\s+(({domain}[^\(]+)\\)?({user}.+?)\("""
  """\sConnected to\s+(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\.-]+))\s+port"""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```