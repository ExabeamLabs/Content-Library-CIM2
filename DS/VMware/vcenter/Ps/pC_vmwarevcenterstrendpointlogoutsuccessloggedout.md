#### Parser Content
```Java
{
Name = vmware-vcenter-str-endpoint-logout-success-loggedout
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ vcenter-server """, """ User """, """ logged out """ ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s+({host}[\w\-.]+)\s""",
    """({service_name}vcenter-server)""",
    """({event_name}logged out)""",
    """User (({domain}[^\\@\(]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s""",
    """user agent: ({user_agent}.*?)\)("|$)""",
    """logged out \(({additional_info}.*?)\)("|$)"""
  ]
  DupFields = [ "event_name->result" ]
  ParserVersion = "v1.0.0"


}
```