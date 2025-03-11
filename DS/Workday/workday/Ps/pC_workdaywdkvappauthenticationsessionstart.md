#### Parser Content
```Java
{
Name = workday-wd-kv-app-authentication-sessionstart
    Vendor = Workday
    Product = Workday
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"Authentication_Type":"""", """"Account_Locked__Disabled_or_Expired":""", """"Session_Start":""" ]
    Fields = [
       """"Account_Locked__Disabled_or_Expired":\s*"({failure_code}[^"]+)"""",
       """"Client_TLS_Version":\s*"({protocol}[^"]+)"""",
       """"Session_Start":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)"""",
       """"Session_ID":\s*"({session_id}[^"]+)"""",
       """"Signon_IP_Address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
       """"Device_Type":\s*"({device_type}[^"]+)"""",
       """"email":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)"""",
       """"Authentication_Type":\s*"({auth_type}[^,]+)"""",
       """"Operating_System":\s*"({os}[^,]+)"""",
       """"Browser_Type":\s*"({user_agent}[^,]+)"""",
       """({app}(W|w)orkday)"""
    ]
    ParserVersion = "v1.0.0"


}
```