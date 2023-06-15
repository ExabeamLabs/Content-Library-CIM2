#### Parser Content
```Java
{
Name = pan-ngfw-csv-http-session-9999
   ParserVersion = v1.0.0
   Vendor = Palo Alto Networks
   Product = Palo Alto NGFW
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   Conditions = [
""",THREAT,url,""",
"""(9999)"""
   ]
   Fields = [
    """({event_category}THREAT)""",
    """({host}[^\s]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,THREAT,url,""",
    """:\d\d:\d\d\s+({host}[\w.-]+)\s""",
    """THREAT,url,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,""",
    """THREAT,url,([^,]*,){5,8}(({domain}[^\\,]+)\\+)?(|({user}[^,]+)),""",
    """THREAT,url,([^,]*,){4}((\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3

}
```