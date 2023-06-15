#### Parser Content
```Java
{
Name = hashicorp-vault-sk4-user-password-reset-success-request
Vendor = HashiCorp
Product = HashiCorp Vault
ParserVersion = "v1.0.0"
TimeFormat = "epoch"
Conditions = [ """"type":"request"""", """"auth":{""", """"operation":"create"""", """"token_type"""", """"vault"""" ]
Fields = [
    """"username":"(hmac-[^"]+|({user}[^"]+))""",
    """"time"+:({time}\d{13})""",
    """"remote_address"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
  ]


}
```