#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-4648-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """subject.logon_id""", """EventID""", """4648""" ]
  Fields = [
    """timestamp"?:"?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"+EventID"+:"+({event_code}\d+)""",
    """"+subject.logon_id"+:"+({login_id}[^"]+)""",
    """"+subject.security_id"+:"+({user_sid}[^"]+)""",
    """"+process_information.process_name"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
    """"+process_information.process_id"+:"+({process_id}[^"]+)""",
    """"+Computer"+:"+({host}[\w\-.]+)""",
    """"+subject.account_name"+:"+(-|({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))""",
    """"+network_information.source_port"+:"+(-|({src_port}\d+))""",
    """"+new_logon.account_domain"+:"+({domain}[^"]+)""",
    """"message"+:"+({additional_info}[^"]+)""",
    """"+ProviderName"+:"+({provider_name}[^"]+)""",
    """"+logon_information.logon_type"+:"+({login_type}\d+)"""
    """account_whose_credentials_were_used.account_domain":"({account_domain}[^"]+)""",
    """account_whose_credentials_were_used.account_name":"({account}[^"]+)""",
    """account_whose_credentials_were_used.logon_guid":"({session_id}[^"]+)""",
    """network_information.network_address:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	]
	ParserVersion = "v1.0.0"


}
```