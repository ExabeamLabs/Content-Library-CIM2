#### Parser Content
```Java
{
Name = "helpsystems-powertechiam-kv-ssh-traffic-success-sshloginsuccess"
  Vendor = "HelpSystems"
  Product = "Powertech Identity and Access Manager"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """sshd - sshlogin"""
    """Successful login"""
  ]
  Fields = [
    """clientTime=\"*({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)Z\"*"""
    """\d\dZ\s+({host}[\w\-.]+)\s+sshd - sshlogin"""
    """user=\"*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
    """ssh [^\s]+ using ({auth}.+?) from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """({event_code}ssh)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```