#### Parser Content
```Java
{
Name = ibm-mainframe-json-app-login-fail-incorrectpassword
   Conditions = [ """"MFSOURCETYPE":"SYSLOG"""", """"MSGTXT":"""", """INCORRECT PASSWORD""" ]
   Fields = ${IBMParsersTemplates.ibm-mainframe-events.Fields}[
     """"MSGTXT":"[^"]+?\sF=({failure_reason}[^"=]+?)(\w+?=|")"""",
     """"MSGTXT":"[^"]+?\sA=({user}[\w\.\-]{1,40}\$?)\sT=""""
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