#### Parser Content
```Java
{
Name = semperis-dsp-str-app-login-success-logindsp
  ParserVersion = v1.0.0
  Vendor = Semperis
  Product = Semperis DSP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """Semperis.DSP""", """[OperationType] LoginDSP""", """[OperationResult] Granted""" ]
  Fields = [
  """OperationTime\]\s({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)"""
  """\w{3,4}\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s({host}[\w\-.]+)"""
  """OperationSource\]\s({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))"""
  """({event_name}DSP Login)"""
  """OperationResult\]\s({action}[^\s]+)"""
  """TrusteeName\]\s(NT AUTHORITY|({domain}[^\\\s]+))[\\]+(SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
  """({app}Semperis.DSP)"""
  """({result}Success)"""
  ]


}
```