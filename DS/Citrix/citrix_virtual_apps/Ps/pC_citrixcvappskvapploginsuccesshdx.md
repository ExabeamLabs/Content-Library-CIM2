#### Parser Content
```Java
{
Name = "citrix-cvapps-kv-app-login-success-hdx"
Vendor = "Citrix"
Product = "Citrix Virtual Apps"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""LogOnStartDate=""""
"""UserName ="""
"""MachineName ="""
"""DeliveryGroup="""
]
Fields = [
"""\sMachineName ="(({domain}[^\\",]+)\\)?({host}[^\\",]+)""""
"""\sLogOnStartDate="({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d\.\d+)"""
"""\sUserName ="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
"""\sClientName ="(-|0+|({src_host}[^",]+?))\s*""""
"""\sClientAddress="(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
"""\sOS_Type="({os}[^",]+)""""
"""\sProtocol="({protocol}[^",]+)""""
]
ParserVersion = "v1.0.0"


}
```