#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-authentication-success-general
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """,SYSTEM,auth,""", """,general,"""]
  Fields = [
    """({host}[\w\-\.]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,auth,""",
    """Client\s'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """,SYSTEM,auth,([^,]+,){2

}
```