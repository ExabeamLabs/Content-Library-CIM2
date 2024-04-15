#### Parser Content
```Java
{
Name = "dell-rsaauthmngr-csv-endpoint-login-fail-auth"
	Vendor = "Dell"
	Product = "RSA Authentication Manager"
	TimeFormat = "yyyy-MM-dd HH:mm:ss"
	Conditions = [
""",AUTH_FAILED_"""
""",FAIL,AUTHN_METHOD_FAILED,"""
	]
	Fields = [
""",({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),AUTH_FAILED_[A-Z_]+,"""
""",({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,AUTH_FAILED_[A-Z_]+,"""
""",({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),[^,]*,AUTH_FAILED_[A-Z_]+,"""
""",({failure_reason}[^,]+),([^,]*,)FAIL,AUTHN_METHOD_FAILED,"""
"""AUTH_FAILED_[A-Z_]+,([^,]*,){7}({user}[^,]+)"""
"""AUTH_FAILED_[A-Z_]+,([^,]*,){12}({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""AUTH_FAILED_[A-Z_]+,([^,]*,){13}({dest_host}[^.,]+)"""
"""AUTH_FAILED_[A-Z_]+,([^,]*,){16}({auth_method}[^.,]+)"""
	]
	ParserVersion = "v1.0.0"


}
```