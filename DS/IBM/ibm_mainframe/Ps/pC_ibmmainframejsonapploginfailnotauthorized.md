#### Parser Content
```Java
{
Name = ibm-mainframe-json-app-login-fail-notauthorized
   ExtractionType = json
   Conditions = [ """"MFSOURCETYPE":"SYSLOG"""", """"MSGTXT":"""", """FACILITY NOT AUTHORIZED""" ]
   Fields = ${IBMParsersTemplates.ibm-mainframe-events.Fields}[
     """exa_json_path=$.MSGTXT,exa_regex=^[^"]+?\sF=({failure_reason}[^"=]+?)(\w+?=|")"""
     """exa_json_path=$.MSGTXT,exa_regex=^[^"]+?\sA=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\sT="""
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