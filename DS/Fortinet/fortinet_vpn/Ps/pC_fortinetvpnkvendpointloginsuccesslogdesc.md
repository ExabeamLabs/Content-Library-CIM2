#### Parser Content
```Java
{
Name = "fortinet-vpn-kv-endpoint-login-success-logdesc"
	Vendor = "Fortinet"
	Product = "Fortinet VPN"
	TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
	Conditions = [
"""action="FSSO-logon"""
""" logdesc="""
	]
	Fields = [
"""date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)"""
"""devname=\"*({host}[^\"]+?)\"*(\s+\w+=|\s*$)"""
"""\ssrcip=\"?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdstip=\"?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\suser=\"*({user}[^\"]+?)\"*(\s+\w+=|\s*$)"""
"""\slogdesc=\"({event_name}[^\"]+)"""
"""\sserver=\"({dest_host}[^\"]+)"""
	]
	ParserVersion = "v1.0.0"


}
```