#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-success-startedsession"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """systemd: Started Session"""
  ]
  Fields = [
    """(\d+|({dest_host}({host}[\w\-.]+)))\s+systemd: Started Session"""
    """of user (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}?\$?))\.?"*$"""
    """({event_code}Started Session)"""
  ]
  ParserVersion = "v1.0.0"


}
```