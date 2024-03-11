#### Parser Content
```Java
{
Name = ibm-mainframe-json-app-login-success-loggedon
   Conditions = [ """"MFSOURCETYPE":"SYSLOG"""", """"MSGTXT":"""", """ LOGGED ON """ ]
   Fields = ${IBMParsersTemplates.ibm-mainframe-events.Fields}[
     """({event_name}LOGGED ON)""",
     """"MSGTXT":"[^"\s]+?\s({user}[^"\s]+)\s\S+?\sLOGGED ON""""
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