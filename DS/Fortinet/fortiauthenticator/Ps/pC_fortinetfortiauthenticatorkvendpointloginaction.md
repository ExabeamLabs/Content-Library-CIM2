#### Parser Content
```Java
{
Name = "fortinet-fortiauthenticator-kv-endpoint-login-action"
	Vendor = "Fortinet"
	Product = "FortiAuthenticator"
	TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
	Conditions = [
"""subcategory="Authentication""""
"""action="Login""""
	]
	Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""nas=\"(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))\""""
"""user=\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
"""status=\"({result}[^\"]+)\""""
"""action=\"({event_name}[^\"]+)\""""
"""status=\"Success\" ({additional_info}.+?)\s*$"""
"""status=\"Failed\" ({failure_reason}.+?)( to .*?)?\s*$""",
"""\Wtz="?({tz}[+-]\d+)"""
	]
	ParserVersion = "v1.0.0"


}
```