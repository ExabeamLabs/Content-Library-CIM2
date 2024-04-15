#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-notification-externalmdm"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
    """ CISE_External_MDM """
	]
  Fields = [
    """({host}\S+) ({event_name}CISE_External_MDM) (\S+\s+){3}({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
    """UserName =({user}[^,]+?),"""
# endpointmacaddress is removed
# operatingsystem is removed
# jailbroken is removed
# manufacturer is removed
# serialnumber is removed
# phonenumber is removed
# servertype is removed
    """UDID=({udid}[^,]+?),"""
# mdmservername is removed
    """SessionId=({session_id}[^,]+?),"""
# ipaddress is removed
  ]
  
  ParserVersion = "v1.0.0"


}
```