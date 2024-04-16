#### Parser Content
```Java
{
Name = semperis-dsp-kv-app-login-logintodsp
  Vendor = Semperis
  Product = Semperis DSP
  TimeFormat = ["dd/MMM/yyyy HH:mm:ss.SSSS","dd/MM/yyyy HH:mm:ss.SSSS"]
  Conditions = [  """Login to DSP""","""Access Granted:""","""Trustee Name:""" ]
  Fields = [
    """Occured at \([^:]+: ({time}\d{2}\/\d{1,2}\/\d{4}\s\d{2}:\d{2}:\d{2}\.\d{4})""",
    """Operation:\s*({event_name}Login to DSP)""",
    """Result:\s*({result}[\S]+)""",
    """Trustee Name:\s*((({domain}[^\\:]+?)|(NT AUTHORITY))\\+)?(({user}[\w\.\-]{1,40}\$?)|(SYSTEM))""",
    """Product:\s*({app}DSP)""",
    """Source:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```