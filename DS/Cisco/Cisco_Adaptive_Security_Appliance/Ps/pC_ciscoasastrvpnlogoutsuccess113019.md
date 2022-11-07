#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-logout-success-113019
   ParserVersion = v1.0.0
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   TimeFormat = "MMM dd yyyy HH:mm:ss"
   Conditions = [ """Session disconnected.""" , """-113019""" ]
   Fields = [
     """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
     """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
     """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+).+?%ASA""",
     """({host}[^\s]+)\s+:\s+%FTD-""",
     """Username[\s\t]+=[\s\t]+(.+?\\)?(?![^\s]+@[^\s]+)(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[^,]+)).+?IP[\s\t]+=[\s\t]+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
     """Username[\s\t]+=[\s\t]+(.+?\\)?({email_address}[^,@]+@[^,@]+).+?IP[\s\t]+=[\s\t]+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
     """\sBytes xmt:\s*({bytes_out}\d+)""",
     """\sBytes rcv:\s*({bytes_in}\d+)""",
     """\sDuration:\s*(({session_day}\d+)d )?({session_hour}\d+)h:({session_min}\d+)m:({session_sec}\d+)s""",
     """%(ASA|FTD)-({priority}\d+)-({event_code}\d+)""",
     """Group = (\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({group_name}[^,]+)),"""
   ]
 

}
```