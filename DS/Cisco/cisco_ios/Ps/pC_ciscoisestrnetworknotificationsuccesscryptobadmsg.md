#### Parser Content
```Java
{
Name = "cisco-ise-str-network-notification-success-cryptobadmsg"
  Vendor = "Cisco"
  Product = "Cisco IOS"
  TimeFormat = "MMM  dd HH:mm:ss"
  Conditions = [ """%CRYPTO-4-IKMP_BAD_MESSAGE:""", """ failed its sanity check """ ]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)"""
    """({event_name}%.+?):"""
    """({event_name}IKE message from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? failed its sanity check or is malformed)"""
  ]
  ParserVersion = "v1.0.0"


}
```