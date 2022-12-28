#### Parser Content
```Java
{
Name = rsa-raa-str-app-register-success-enrollcompleted
  ParserVersion = v1.0.0
  Conditions = [ """AAOP-Audit""", """ENROLL_COMPLETED""" ]

rsa-account-activity = {
  Vendor = RSA
  Product = RSA Adaptive Authentication
  TimeFormat = "yyyy-MM-dd HH:mm:ss,SSS Z"
  Fields = [
    """\s({host}[^\s]+)\s+AAOP-Audit""",
    """\s({host}[^\s]+)\s+AAOP-Audit\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d(,\d+ (\+|-)\d+)?)\s+\|[^\|]+\|\s[^\s]+\s\|\s*\[?({user_id}[^\]\|\s]+)\s+\|\s*([^\s\|]+)\s+\|\s*((?i)DEVID_UNDEFINED|({device_id}[^\s\|]+))\s+\|\s((?i)IP_UNDEFINED|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\|\s*([^\|]+)\s+\|\s*({event_name}[^\|]+)\s+\|\s*((?i)EVENTID_UNDEFINED|({event_code}[^\|]+))\s+\|\s*((?i)TRANSID_UNDEFINED|({transaction_id}[^\|]+))\s+\|\s*((?i)TRANSTYPE_UNDEFINED|({transaction_type}[^\|]+))\s+\|\s*""", #dl field removed
  
}
```