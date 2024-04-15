#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-success-4624-5"
Conditions = [
""""data.id":"4624""""
""""type":"wazuh-alerts""""
""""decoder.parent":"windows""""
]
ParserVersion = "v1.0.0"

wazuh-windows-template.Fields} [
    """Type d\\u2019ouverture de session\\u00A0:\s*({login_type}\d+)""",
    """Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}[^\s]+))\s*Adresse du r\\u00E9seau source\\u00A0:""",
    """Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^\s]+))\s*Adresse du r\\u00E9seau source\\u00A0:\s*-\s+""",
    """Adresse du r\\u00E9seau source\\u00A0:\s*(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Port source\\u00A0:""",
    """Processus d\\u2019ouverture de session\\u00A0:\s*({auth_process}[^\s]+)\s*Package d\\u2019authentification\\u00A0:\s*({auth_package}[^\s]+)""",
    """\s*Compte pour lequel l\\u2019ouverture de session a \\u00E9chou\\u00E9\\u00A0:\s*ID de s\\u00E9curit\\u00E9\\u00A0:\s*(?:\/?NULL SID|({user_sid}.+?))\s*Nom du compte\\u00A0""",
    """ouverture de session a \\u00E9chou\\u00E9\\u00A0:.+?Domaine du compte\\u00A0:\s*(?=\w)({domain}.+?)\s*Informations sur l\\u2019\\u00E9chec\\u00A0""",
    """ouverture de session a \\u00E9chou\\u00E9\\u00A0:.+?Nom du compte\\u00A0:\s*(?=\w)({user}.+?)\s*Domaine du compte\\u00A0:""",
    """Raison de l\\u2019\\u00E9chec\\u00A0:\s*({failure_reason}.+?)\s*\\u00C9tat\\u00A0:""",
    """Sujet.+?Nom du compte\\u00A0:\s*(?=\w)({src_user}.+?)\s*Domaine du compte\\u00A0:""",
    """Sujet.+?Domaine du compte\\u00A0:\s*(?=\w)({src_domain}[^:]+?)\\s*ID d\\u2019ouverture de session\\u00A0:""",
    """\s*Sous-\\u00E9tat\\u00A0:\s*({result_code}.+?)\s*Informations sur le processus\\u00A0:"""
    ]
    DupFields = [
      "result_code->failure_code"
    
}
```