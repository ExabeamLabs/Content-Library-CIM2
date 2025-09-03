#### Parser Content
```Java
{
Name = ibm-mainframe-json-app-logout-success-loggedoff
   Vendor = IBM
   Product = IBM Mainframe
   TimeFormat = "yyyy-MM-dd HH:mm:ss.SS Z"
   Conditions = [ """"MFSOURCETYPE":"SYSLOG"""", """"MSGTXT":"""", """ LOGGED OFF """ ]
   Fields = [
     """"DATETIME":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+?\s(\+|-)\d{4}?)"""",
     """"ACTION":"({severity}[^"]+?)"""",
     """"MSGNUM":"({event_code}[^"]+?)"""",
     """"MSGTXT":"({additional_info}[^"]+?)"""",
     """({event_name}LOGGED OFF)""",
     """"MSGTXT":"[^"\s]+?\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\S+?\sLOGGED OFF"""
     """"MSGTXT":"({additional_info}[^"]+?)""""
   ]
   DupFields = ["event_name->operation"]
   ParserVersion = "v1.0.0"


}
```