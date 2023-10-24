#### Parser Content
```Java
{
Name = "fortinet-fortiauthenticator-kv-endpoint-login-success-0102043039"
	Vendor = "Fortinet"
	Product = "FortiGate"
	TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
	Conditions = [
""" logid="0102043039" """
	]
	Fields = [
"""date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)"""
"""devname=\"*({host}[^\"]+?)\"*(\s+\w+=|\s*$)"""
"""\ssrcip=\"?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\suser=\"*(host\/({src_host}[\w\-.]+)|({email_address}[^"@]+@[^\."]+\.[^"]+)|({user}[\w\.\-]{1,40}\$?)@({domain}[^"]+)|((({=domain}[^\\"]+)\\+)?({=user}[^"]+)))\"*"""
"""\slogdesc=\"({event_name}[^\"]+)"""
"""\smsg=\"({additional_info}[^\"]+)"""
"""authserver=\"+(N/A|({auth_server}[^"]+))""",
"""\Wtz="?({tz}[+-]\d+)"""
	]
	ParserVersion = "v1.0.0"


}
```