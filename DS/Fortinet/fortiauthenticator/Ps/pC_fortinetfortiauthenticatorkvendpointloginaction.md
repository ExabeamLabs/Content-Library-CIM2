#### Parser Content
```Java
{
Name = "fortinet-fortiauthenticator-kv-endpoint-login-action"
	Vendor = "Fortinet"
	Product = "FortiAuthenticator"
	TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
	Conditions = [
"""subcategory="Authentication""""
"""action="Login""""
	]
	Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""nas=\"({dest_host}[^\"]+)\""""
"""user=\"({user}[^\"]+)\""""
"""status=\"({result}[^\"]+)\""""
"""action=\"({event_name}[^\"]+)\""""
"""status=\"Success\" ({additional_info}.+?)\s*$"""
"""status=\"Failed\" ({failure_reason}.+?)( to .*?)?\s*$"""
	]
	ParserVersion = "v1.0.0"


}
```