#### Parser Content
```Java
{
Name = "lastpass-l-sk4-app-login-success-actionlogin"
  Vendor = "LastPass"
  Product = "LastPass"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """Action":"Log in"""
    """dproc=EventReporting"""
    """destinationServiceName =LastPass"""
  ]
  Fields = [
    """\"Time\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """\"IP_Address\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
    """destinationServiceName =({app}[^=]+?)\s\w+="""
    """\"+Action\"+:\"+({action}[^\"]+)\"+"""
    """\"Username\"+:\"+({email_address}[^@]+@[^\.\"]+\.[^\"]+)"""
    """\"+Data\"+:\"+({additional_info}[^\"\}]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```