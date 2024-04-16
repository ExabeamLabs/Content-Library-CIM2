#### Parser Content
```Java
{
Name = "dell-rsaauthmngr-str-endpoint-login-success-ucm"
	Vendor = "RSA"
	Product = "RSA Authentication Manager"
	TimeFormat = "yyyy-MM-dd HH:mm:ss"
	Conditions = [
""",UCM_REQUEST_AUTO_APPROVE,"""
""",SUCCESS,"""
	]
	Fields = [
""",({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),UCM_REQUEST_AUTO_APPROVE"""
""",({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,[^,]*,UCM_REQUEST_AUTO_APPROVE"""
"""UCM_REQUEST_AUTO_APPROVE,([^,]*,){8}({user}[\w\.\-]{1,40}\$?)"""
"""UCM_REQUEST_AUTO_APPROVE,([^,]*,){15}({dest_host}[^.,]+)"""
"""UCM_REQUEST_AUTO_APPROVE,([^,]*,){21}({auth_method}[^\s,]+)"""
	]
	ParserVersion = "v1.0.0"


}
```