#### Parser Content
```Java
{
Name = netwrix-ntp-kv-endpoint-authentication-success
  ParserVersion = "v1.0.0"
  Vendor = Netwrix
  Product = Netwrix Threat Prevention
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ Netwrix Threat Prevention """, """ Kerberos Login succeed """, """ Event_Source=""", """BlockedEvent=""", """SuccessfulChange=""" ]
  Fields = [
	"""({time}\w+\s\d\d\s\d\d:\d\d:\d\d)\s\S+\sNetwrix Threat Prevention""",
	"""({event_name}Kerberos Login succeed)""",
	"""PolicyName ="({policy_name}[^"]+)"""",
	"""Server="(({domain}[^"\\]+)\\)?({dest_host}[\w\-\.]+)"""",
	"""ServerAddress="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
	"""Perpetrator="(({domain}[^"\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
	"""Domain="({domain}[^"]+)"""",
	"""ClientAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
	"""DistinguishedName ="({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+))""""
  ]


}
```