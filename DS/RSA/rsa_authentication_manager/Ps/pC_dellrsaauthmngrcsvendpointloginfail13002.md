#### Parser Content
```Java
{
Name = "dell-rsaauthmngr-csv-endpoint-login-fail-13002"
	Vendor = "RSA"
	Product = "RSA Authentication Manager"
	TimeFormat = "yyyy-MM-dd HH:mm:ss"
	Conditions = [
""",AUTHN_LOGIN_EVENT,13002,FAIL,"""
	]
	Fields = [
""",({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),AUTHN_LOGIN_EVENT"""
""",({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,AUTHN_LOGIN_EVENT"""
""",({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,AUTHN_LOGIN_EVENT"""
""",FAIL,({failure_reason}[^,]+)"""
"""AUTHN_LOGIN_EVENT,([^,]*,){7}({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""AUTHN_LOGIN_EVENT,([^,]*,){12}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""AUTHN_LOGIN_EVENT,([^,]*,){13}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)),"""
"""AUTHN_LOGIN_EVENT,([^,]*,){16}({auth_method}[^.,]+)"""
"""\d+-\d+-\d+\s\d+:\d+:\d+,([^,]*,)\s*({domain}[^,]+),"""
	]
	ParserVersion = "v1.0.0"


}
```