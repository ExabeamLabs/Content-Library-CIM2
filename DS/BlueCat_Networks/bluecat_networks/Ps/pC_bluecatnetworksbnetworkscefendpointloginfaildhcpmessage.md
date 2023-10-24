#### Parser Content
```Java
{
Name = "bluecatnetworks-bnetworks-cef-endpoint-login-fail-dhcpmessage"
	Vendor = "BlueCat Networks"
	Product = "BlueCat Networks"
	TimeFormat = "epoch"
	Conditions = [
		"""CEF:"""
		"""|BCN|BDDS_DHCP|"""
		"""|DHCP_Message|DHCP message|"""
		"""src="""
	]
	Fields = [
		"""\srt=({time}\d{13})"""
		"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
		"""\sdvchost=({dest_host}[\w.\-]+)"""
		"""\scat=(?:|({category}.+?))\s\w+="""
		"""\sshost=({dest_host}[^\s]+)"""
		"""\ssrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
		"""originalAgentHostName =({host}[^"]+)\soriginalAgentAddress"""
		"""originalAgentAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
		"""originalAgentMacAddress=({src_mac}[^\s]+)"""
	]
	ParserVersion = "v1.0.0"


}
```