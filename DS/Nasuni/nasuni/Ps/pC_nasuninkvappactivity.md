#### Parser Content
```Java
{
Name = "nasuni-n-kv-app-activity"
	Vendor = "Nasuni"
	Product = "Nasuni"
	TimeFormat = "epoch_sec"
	Conditions = [""""event_type":""", """"proto":""", """"resource":""", """nasuni."""]
	Fields = [
		"""({host}\S+)\s*nasuni""",
		""""timestamp":\s*({time}\d{10})""",
		""""event_type":\s*"({event_name}[^"]+)"""",
		""""ipaddr":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
		""""groupname":\s*"(({domain}[^\\"]+)\\+)?({group_name}[^"]+)""""
    """"username":\s*"(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
		""""path":\s*"({file_path}({file_dir}[^"\|][^\|,]*?[\\\/]+)?(|({file_name}[^\\\/\|]*?(\.({file_ext}\w+))?)))"""",
    """"newpath":\s*(null|"({file_path}({file_dir}[^"\|][^\|,]*?[\\\/]+)?(|({file_name}[^\\\/\|]*?(\.({file_ext}\w+))?)))")""",
		""""resource":\s*"({resource_name}[^"]+)"""",
		""""result":\s*({result}\d+)""",
		""""proto":\s*"AUDIT_PROTO_({protocol}[^"]+)"""",
		""""sid":\s*"({user_sid}[^"]+)"""",
		""""name":\s*"({attribute}[^"]+)"""
	]
	ParserVersion = "v1.0.0"


}
```