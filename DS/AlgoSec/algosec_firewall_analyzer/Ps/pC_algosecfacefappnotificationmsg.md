#### Parser Content
```Java
{
Name = algosec-fa-cef-app-notification-msg
 Product = AlgoSec Firewall Analyzer
 Vendor = AlgoSec
 ParserVersion = v1.0.0
 TimeFormat ="yyyy-MM-dd HH:mm:ss"
 Conditions = [ """CEF:""", """|AlgoSec|Firewall Analyzer|""", """msg=""" ]
 Fields =[
   """({host}[^\s]+)\s+:\s+CEF""",
   """CEF:\d+\|([^\|]+\|){2}({version}[^\|]+)""",
# log_level is removed
   """CEF:\d+\|([^\|]+\|){5}({alert_severity}[^\|]+)""",
   """CEF:\d+\|([^\|]+\|){7}\s*msg=({additional_info}.+?)\s*$"""
 ]


}
```