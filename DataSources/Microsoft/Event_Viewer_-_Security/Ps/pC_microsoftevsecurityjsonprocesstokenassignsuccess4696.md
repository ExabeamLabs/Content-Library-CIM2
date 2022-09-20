#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-token-assign-success-4696
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """subject.logon_id""", """EventID""", """4696""" ]
  Fields = [
    """"+EventID"+:"+({event_code}\d+)""",
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}Z)"""
    """"+subject.logon_id"+:"+({login_id}[^"]+)""",
    """"+subject.security_id"+:"+({user_sid}[^"]+)""",
    """"+process_information.process_name"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
    """"+process_information.process_id"+:"+({process_id}[^"]+)""",
    """"+Computer"+:"+({host}[^"]+)""",
    """"+subject.account_name"+:"+(-|({email_address}({user}[^@]+)@({domain}[^"]+))|({=user}[^"]+))""",
    """"+network_information.source_port"+:"+(-|({src_port}\d+))""",
    """account_domain"+:"+({domain}[^"]+)""",
    """"message"+:"+({additional_info}[^"]+)""",
    """"+ProviderName"+:"+({provider_name}[^"]+)""",
# token_account_name is removed
# token_sid is removed
# token_domain is removed
  ]


}
```