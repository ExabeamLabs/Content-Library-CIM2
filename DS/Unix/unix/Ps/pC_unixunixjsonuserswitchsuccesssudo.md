#### Parser Content
```Java
{
Name = unix-unix-json-user-switch-success-sudo
Product = "Unix"
ExtractionType = json
Conditions = [
  """"decoder.parent":"sudo""""
  """"type":"wazuh-alerts""""
]
ParserVersion = "v1.0.0"

wazuh-windows-template.Fields} [
    """exa_regex=Type d\\u2019ouverture de session\\u00A0:\s*({login_type}\d+)""",
    """exa_regex=Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}[^\s]+))\s*Adresse du r\\u00E9seau source\\u00A0:""",
    """exa_regex=Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^\s]+))\s*Adresse du r\\u00E9seau source\\u00A0:\s*-\s+""",
    """exa_regex=Adresse du r\\u00E9seau source\\u00A0:\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Port source\\u00A0:""",
    """exa_regex=Processus d\\u2019ouverture de session\\u00A0:\s*({auth_process}[^\s]+)\s*Package d\\u2019authentification\\u00A0:\s*({auth_package}[^\s]+)""",
    """exa_regex=\s*Compte pour lequel l\\u2019ouverture de session a \\u00E9chou\\u00E9\\u00A0:\s*ID de s\\u00E9curit\\u00E9\\u00A0:\s*(?:\/?NULL SID|({user_sid}.+?))\s*Nom du compte\\u00A0""",
    """exa_regex=ouverture de session a \\u00E9chou\\u00E9\\u00A0:.+?Domaine du compte\\u00A0:\s*(?=\w)({domain}.+?)\s*Informations sur l\\u2019\\u00E9chec\\u00A0""",
    """exa_regex=ouverture de session a \\u00E9chou\\u00E9\\u00A0:.+?Nom du compte\\u00A0:\s*(?=\w)({user}[\w\.\-]{1,40}\$?)\s*Domaine du compte\\u00A0:""",
    """exa_regex=Raison de l\\u2019\\u00E9chec\\u00A0:\s*({failure_reason}.+?)\s*\\u00C9tat\\u00A0:""",
    """exa_regex=Sujet.+?Nom du compte\\u00A0:\s*(?=\w)({src_user}.+?)\s*Domaine du compte\\u00A0:""",
    """exa_regex=Sujet.+?Domaine du compte\\u00A0:\s*(?=\w)({src_domain}[^:]+?)\\s*ID d\\u2019ouverture de session\\u00A0:""",
    """exa_regex=\s*Sous-\\u00E9tat\\u00A0:\s*({result_code}.+?)\s*Informations sur le processus\\u00A0:"""
    ]
    DupFields = [
      "result_code->failure_code"
    
}
```