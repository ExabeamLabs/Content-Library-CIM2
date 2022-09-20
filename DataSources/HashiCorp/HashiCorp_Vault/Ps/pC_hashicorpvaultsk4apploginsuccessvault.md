#### Parser Content
```Java
{
Name = hashicorp-vault-sk4-app-login-success-vault
  ParserVersion = "v1.0.0"
  Vendor = HashiCorp
  Product = HashiCorp Vault
  TimeFormat = "epoch"
  Conditions = [ """"type":"request"""", """"auth":{""", """"token_type"""", """"ttam_service":"vault"""" ]
  Fields = [
    """"username"+:"+({user}[^"]+)""",
    """"time"+:({time}\d+)""",
    """"remote_address"+:"+({src_ip}[^"]+)""",
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