#### Parser Content
```Java
{
Name = "zoom-z-sk4-app-login-success-signin"
  Vendor = "Zoom"
  Product = "Zoom"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
    """"type":"Sign in""""
    """destinationServiceName =Zoom"""
  ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)"""
    """time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
    """\"type\":\"({operation}[^\"]+)\""""
    """\"email\":\"({email_address}[^\"]+)\""""
    """\Wmsg=({additional_info}.+?)(\s+\w+=|\s*$)"""
    """\"ip_address\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
    """\"client_type\"\s*:\s*\"({client_type}[^\"]+)\""""
    """\"version\"\s*:\s*\"({app_version}[^\"]+)\""""
  ]
  ParserVersion = "v1.0.0"


}
```