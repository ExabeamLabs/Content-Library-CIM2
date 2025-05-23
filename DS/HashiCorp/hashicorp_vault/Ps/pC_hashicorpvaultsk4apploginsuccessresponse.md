#### Parser Content
```Java
{
Name = hashicorp-vault-sk4-app-login-success-response
Vendor = HashiCorp
Product = HashiCorp Vault
ParserVersion = "v1.0.0"
TimeFormat = ["epoch", "epoch_sec"]
Conditions = [ """"type":"response"""", """"auth":{""", """"operation":"""", """"token_type"""", """"vault"""" ]
Fields = [
    """"username":"(hmac-[^"]+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"time"+:({time}\d{10,13})""",
    """"remote_address"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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