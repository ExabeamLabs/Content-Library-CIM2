#### Parser Content
```Java
{
Name = hashicorp-vault-sk4-user-password-reset-success-request
ParserVersion = "v1.0.0"
Conditions = [ """"type":"request"""", """"auth":{""", """"operation":"create"""", """"token_type"""", """"ttam_service":"vault"""" ]

hashicorp-login-activity {
    Vendor = HashiCorp
    Product = HashiCorp Vault
    TimeFormat = "epoch"
    Fields = [
      """"username":"(hmac-[^"]+|({user}[^"]+))""",
      """"time"+:({time}\d+)""",
      """"remote_address"+:"+({src_ip}[^"]+)""",
      """"operation"+:"+({operation}[^"]+?)",""",
      """"path"+:"+({path}[^"]+?)",""",
      """"type"+:"(hmac-[^"]+|({category}[^"]+?))",""",
      """"client_token"+:"+({client_token}[^"]+?)",""",
      """\srequestClientApplication=({app}[^=]+?)\s*\w+=""",
      """"entity_id"+:"+({vault_entity_id}[^"]+?)",""",
      """"accessor"+:"+({accessor}[^"]+?)",""",
      """"policies"+:\[({policies}[^\]]+?)\]""",
      """metadata":\{"([^,]+,){2}"role":"({role}[^"]+)""",
      """"user-agent":\["({user_agent}[^"]+)""",
    
}
```