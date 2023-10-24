#### Parser Content
```Java
{
Name = forcepoint-casb-csv-http-session-success
  Vendor = Forcepoint
  Product = Forcepoint CASB
  TimeFormat = "dd/MM/yyyy HH:mm:ss"
  Conditions = [ ""","forcepoint.io",""", ""","Allowed",""", ""","Static Classification",""" ]
  Fields=[
    ""","({host}[^":]+)(:\d+\/)?","({action}[^"]+)","({category}[^"]+)","([^,]+,){2,3}"({categories}[^"]+)","({src_host}[^@,]+)(@[^,]+),"[^"]+","forcepoint.io""""
    """"forcepoint.io",([^,]+,){4}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","(Not available|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))",([^,]+,){3}"({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)",([^,]+,){5}"({user_agent}[^"]+)",([^,]+,){2}"({http_response_code}\d+)"""
     ]
  ParserVersion = "v1.0.0"


}
```