#### Parser Content
```Java
{
Name = f5-bigip-kv-configuration-modify-audit
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss" , "MMM dd HH:mm:ss" ]
  Conditions = [ """tmsh[""", """ - pid=""", """ user=""", """ folder=""", """ status=""", """ cmd_data=""",  """: AUDIT """ ]
  Fields = [
    """<(?:\d{1,3})>(?:\d{0,2}\s)?({time}\w{3}\s+\d{1,2}\s+\d{2}:\d{2}:\d{2})"""
    """({host}[\w.-]+)\snotice""",
    """pid=({process_id}\d+)""",
    """user=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """cmd_data=({additional_info}.+?)\s+($|\w+=)""",
    """tmsh\[\d+\]:\s+({activity_id}\d+):""", 
    """\sstatus=\[({status_msg}[^\]]+)\]\s""",
    """cmd_data=({command}.*?)\s*$"""
  ]


}
```