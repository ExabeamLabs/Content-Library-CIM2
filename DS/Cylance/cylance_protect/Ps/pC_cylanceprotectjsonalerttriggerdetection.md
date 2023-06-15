#### Parser Content
```Java
{
Name = cylance-protect-json-alert-trigger-detection
  ParserVersion = v1.0.0
  Vendor = Cylance
  Product = Cylance PROTECT
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """The Cosmopolitan of Las Vegas""", """Background Detection""", """"Last Reported User":""" ]
  Fields =[
    """"Created"+:\s+"+({time}\d+\/\d+\/\d+\s\d+:\d+:\d+\s\w+)""",
    """"Device Name"+:\s+"+({host}\w+)""",
    """"IP Addresses"+:\s"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"Last Reported User"+:\s"+(({domain}[^\\\/,]+)?[\\\/]+)?({user}[^",]+)""",
    """"Serial Number"+:\s+"+({alert_id}[^",]+)""",
    """"Policy"+:\s+"+({alert_name}[^",]+)""",
    """"Background Detection"+:\s*"+(N\/A|({direction}[^",]+))""",
# is_online is removed
# offline_date is removed
# online_date is removed
    """"Zones"+:\s*"+(N\/A|({zone}[^",]+))"""
  ]


}
```