#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-process-token-assign-success-4696
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """subject.logon_id""", """EventID""", """4696""" ]
  Fields = [
    """exa_json_path=$..EventID,exa_field_name=event_code""",
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$..['subject.logon_id'],exa_field_name=login_id""",
    """exa_json_path=$..['subject.security_id'],exa_field_name=user_sid""",
    """exa_json_path=$..['process_information.process_name'],exa_regex=^({process_path}({process_dir}[^"]*?)\\+({process_name}[^"\\\/]+))$""",
    """exa_json_path=$..['process_information.process_id'],exa_field_name=process_id""",
    """exa_json_path=$..Computer,exa_regex=^({host}[\w\-.]+)$""",
    """exa_json_path=$..['subject.account_name'],exa_regex=^(-|({email_address}({user}[\w\.\-]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))$""",
    """exa_json_path=$..['subject.account_domain'],exa_field_name=domain""",
    """exa_json_path=$..message,exa_field_name=additional_info""",
    """exa_json_path=$..ProviderName,exa_field_name=provider_name"""
# token_account_name is removed
# token_sid is removed
# token_domain is removed
  ]


}
```