#### Parser Content
```Java
{
Name = ibm-mainframe-json-user-disable-success-suspendedon
   Conditions = [ """"MFSOURCETYPE":"SYSLOG"""", """"MSGTXT":"""", """ was suspended on """ ]
   Fields = ${IBMParsersTemplates.ibm-mainframe-events.Fields}[
     """({event_name}suspended)""",
     """"MSGTXT":"[^"]+?\sUserID ({user}[^"\s]+)\sfor""""
   ]
   ParserVersion = "v1.0.0"

ibm-mainframe-events {
    Vendor = IBM
    Product = IBM Mainframe
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SS Z"
    Fields = [ 
      """"DATETIME":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d{2}\s(\+|\-)\d{4}?)"""",
	  """"ACTION":"({severity}[^"]+?)"""", 
      """"MSGNUM":"({event_code}[^"]+?)"""",
      """"MSGTXT":"({additional_info}[^"]+?)"""" 
    
}
```