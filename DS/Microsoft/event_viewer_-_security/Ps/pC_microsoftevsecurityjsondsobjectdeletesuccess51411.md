#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-delete-success-5141-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ExtractionType = json
TimeFormat = ["MMM dd HH:mm:ss yyyy", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd HH:mm:ss Z"]
Conditions = [ """A directory service object was deleted""", """"EventID":5141""", """"Channel":"Security"""" ]
Fields = [
  """exa_json_path=$.TimeCreated,exa_field_name=time"""
  """exa_json_path=$.ProcessID,exa_field_name=process_id"""
  """exa_json_path=$.ProviderName,exa_field_name=provider_name"""
  """exa_json_path=$.EventID,exa_field_name=event_code"""
  """exa_regex=({event_name}A directory service object was deleted)"""
  """exa_json_path=$.Keywords,exa_field_name=result"""
  """exa_json_path=$.Computer,exa_field_name=host"""
  """exa_regex=Subject:.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)"""
  """exa_regex=Subject: Security ID:\s*({user_sid}[^\s]+)"""
  """exa_regex=Object:.+?Class:\s+({object_type}.+?)\s+Operation:""",
  """exa_regex=Object:\s+DN:\s+({ds_object_dn}.+?)\s+GUID:""",
  """exa_regex=Object:\s+DN:.+?({ds_object_ou}OU.+?)\s+GUID:"""
  """exa_regex=Directory Service:\s*Name(:|=)\s*({ds_name}[^\s]+)\s*.*?Type(:|=)\s*({ds_type}.*?Services)"""
]
ParserVersion = "v1.0.0"


}
```