#### Parser Content
```Java
{
Name = "securelink-s-str-app-login-success-connected"
  Vendor = "SecureLink"
  Product = "SecureLink"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """SecureLink"""
    """ AUDIT"""
    """ connected to Application """
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+({host}[\w\-\.]+)\s"""
    """connected to Application ({app}[^\."]+)"""
    """\sAUDIT.+?\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\)"""
    """({event_name}connected to Application)"""
  ]
  ParserVersion = "v1.0.0"


}
```