#### Parser Content
```Java
{
Name = "dell-rsaauthmngr-csv-identitysourcecleanupcontrollerimpl"
	Vendor = "RSA"
	Product = "RSA Authentication Manager"
	TimeFormat = "yyyy-MM-dd HH:mm:ss"
	Conditions = [ """,CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_""", """IdentitySourceCleanupControllerImpl, """ ]
	Fields = [
			""",({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_[A-Z_]+,""",
			""",({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?,CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_[A-Z_]+,""",
			""",({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),[^,]*,CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_[A-Z_]+,""",
			"""CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_[A-Z_]+,([^,]*,){8}({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
			"""CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_[A-Z_]+,({event_code}\d+)""",
			"""CLEANUP_UNRESOLVED_USERS_IS_UNSPECIFIED_[A-Z_]+,[^,]*,({result}[^,]+),"""
	]
	ParserVersion = "v1.0.0"


}
```