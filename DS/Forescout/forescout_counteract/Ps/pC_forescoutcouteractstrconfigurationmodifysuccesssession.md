#### Parser Content
```Java
{
Name = "forescout-couteract-str-configuration-modify-success-session"
Vendor = "Forescout"
Product = "Forescout CounterACT"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
Conditions = [
""" User """
""" session """
""" Details: """
""" Main Appliance["""
]
Fields = [
"""(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s+Main Appliance"""
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""\sUser\s+({user}[\w\.\-]{1,40}\$?)\s+session\s+({session_id}\d+)\s+({operation}\w+)\s+({object}.+?)\."""
"""\sDetails:\s*({additional_info}.+?)(\s+device\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)?\s*$"""
"""from\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+to\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]"""
]
ParserVersion = "v1.0.0"


}
```