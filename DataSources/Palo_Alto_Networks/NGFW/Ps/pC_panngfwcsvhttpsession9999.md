#### Parser Content
```Java
{
Name = pan-ngfw-csv-http-session-9999
   ParserVersion = v1.0.0
   Vendor = Palo Alto Networks
   Product = NGFW
   TimeFormat = "yyyy/MM/dd HH:mm:ss"
   Conditions = [
""",THREAT,url,""",
"""(9999)"""
   ]
   Fields = [
    """({host}[^\s]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,THREAT,url,""",
    """:\d\d:\d\d\s+({host}[\w.-]+)\s""",
    """THREAT,url,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),({src_ip}[a-fA-F\d.:]+),({dest_ip}[a-fA-F\d.:]+),""",
    """THREAT,url,([^,]*,){5,8}(({domain}[^\\,]+)\\+)?(|({user}[^,]+)),""",
    """THREAT,url,([^,]*,){4}((\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3

}
```