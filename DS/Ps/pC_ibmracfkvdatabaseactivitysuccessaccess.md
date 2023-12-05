#### Parser Content
```Java
{
Name = ibm-racf-kv-database-activity-success-access
Conditions = [
  """EVNTPRODESCR=VANGUARD_ACTIVE_ALERTS"""
  """EVNTNAME=Access"""
  """EVNTTEXT=Failed due to PROTECTALL"""
]
ParserVersion = "v1.0.0"

SS Z"
    Fields = [ 
      """"DATETIME":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d{2}\s(\+|\-)\d{4}?)"""",
	  """"ACTION":"({severity}[^"]+?)"""", 
      """"MSGNUM":"({event_code}[^"]+?)"""",
      """"MSGTXT":"({additional_info}[^"]+?)"""" 
    
}
```