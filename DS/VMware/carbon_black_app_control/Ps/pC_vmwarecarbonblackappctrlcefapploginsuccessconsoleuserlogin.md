#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-cef-app-login-success-consoleuserlogin"
Vendor = "VMware"
Product = "Carbon Black App Control"
TimeFormat = "MM dd yyyy HH:mm:ss"
Conditions = [
"""|Bit9|Security Platform|"""
"""|Console user login|"""
]
Fields = [
"""({time}\d\d \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
"""(\||\s)dst=(|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)(\s+[\w-]+=|\s*$)"""
"""(\||\s)duser=(|({domain}[^\s\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)"""
"""(\||\s)dvchost=(|({host}.+?))(\s\w+=|\s*$)"""
"""(\||\s)msg=.+from\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```