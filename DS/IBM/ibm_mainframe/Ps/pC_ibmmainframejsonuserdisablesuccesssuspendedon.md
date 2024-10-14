#### Parser Content
```Java
{
Name = ibm-mainframe-json-user-disable-success-suspendedon
   ExtractionType = json
   Conditions = [ """"MFSOURCETYPE":"SYSLOG"""", """"MSGTXT":"""", """ was suspended on """ ]
   Fields = ${IBMParsersTemplates.ibm-mainframe-events.Fields}[
     """exa_regex=({event_name}suspended)""",
     """exa_json_path=$.MSGTXT,exa_regex=^[^"]+?\sUserID ({user}[\w\.\-\!\#\^\~]{1,40}\$?)\sfor"""
   ]
   ParserVersion = "v1.0.0"

ibm-mainframe-events {
    Vendor = IBM
    Product = IBM Mainframe
    TimeFormat = "yyyy-MM-dd HH:mm:ss.SS Z"
    Fields = [
      """exa_json_path=$.DATETIME,exa_field_name=time""",
      """exa_json_path=$.ACTION,exa_field_name=severity""",
      """exa_json_path=$.MSGNUM,exa_field_name=event_code""",
      """exa_json_path=$.MSGTXT,exa_field_name=additional_info"""
    
}
```