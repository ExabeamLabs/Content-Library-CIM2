#### Parser Content
```Java
{
Name = f5-bigip-kv-configuration-modify-audit
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ tmsh[""", """ - pid=""", """ user=""", """ folder=""", """ status=""", """ cmd_data=""",  """: AUDIT """ ]
  Fields = [
    """({host}[^\s]+)\snotice""",
    """pid=({event_code}\d+)""",
    """user=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
    """cmd_data=({additional_info}.+?)\s+($|\w+=)""",
  ]


}
```