#### Parser Content
```Java
{
Name = hashicorp-vault-sk4-app-login-success-vault
  ParserVersion = "v1.0.0"
  Vendor = HashiCorp
  Product = HashiCorp Vault
  TimeFormat = "epoch_sec"
  Conditions = [ """"type":"request"""", """"auth":{""", """"token_type"""", """"ttam_service":"vault"""" ]
  Fields = [
    """"username"+:"+({user}[^"]+)""",
    """"time"+:({time}\d{10})""",
    """"remote_address"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"operation"+:"+({operation}[^"]+)""",
    """"path"+:"+({path}[^"]+)""",
    """"type"+:"+({category}[^"]+)""",
    """"client_token"+:"+({client_token}[^"]+)""",
    """\srequestClientApplication=({app}.+?)\s*\w+=""",
    """"entity_id"+:"+({vault_entity_id}[^"]+)""",
    """"accessor"+:"+({accessor}[^"]+)""",
    """"policies"+:\[({policies}.+?)\]""",
  ]


}
```