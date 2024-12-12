#### Parser Content
```Java
{
Name = wazuh-evsecurity-kv-endpoint-login-fail-4625
  ParserVersion = v1.0.0
  Product = Wazuh
  Conditions = [ """"data.id":"4625"""", """"type":"wazuh-alerts"""", """"decoder.parent":"windows""""  ]
    Fields = ${WazuhParserTemplates.wazuh-windows-template.Fields} [
    """exa_json_path=$.['data.system_name'],exa_regex=^({host}[\w\-.]+)$""",
    """exa_regex=Type d\\u2019ouverture de session\\u00A0:\s*({login_type}\d+)""",
    """exa_regex=Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host_windows}[^\s]+))\s*Adresse du r\\u00E9seau source\\u00A0:""",
    """exa_regex=Nom de la station de travail\\u00A0:\s*(-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^\s]+))\s*Adresse du r\\u00E9seau source\\u00A0:\s*-\s+""",
    """exa_regex=Adresse du r\\u00E9seau source\\u00A0:\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Port source\\u00A0:""",
    """exa_regex=Processus d\\u2019ouverture de session\\u00A0:\s*({auth_process}[^\s]+)\s*Package d\\u2019authentification\\u00A0:\s*({auth_package}[^\s]+)""",
    """exa_regex=\s*Compte pour lequel l\\u2019ouverture de session a \\u00E9chou\\u00E9\\u00A0:\s*ID de s\\u00E9curit\\u00E9\\u00A0:\s*(?:\/?NULL SID|({user_sid}.+?))\s*Nom du compte\\u00A0""",
    """exa_regex=ouverture de session a \\u00E9chou\\u00E9\\u00A0:.+?Domaine du compte\\u00A0:\s*(?=\w)({domain}.+?)\s*Informations sur l\\u2019\\u00E9chec\\u00A0""",
    """exa_regex=ouverture de session a \\u00E9chou\\u00E9\\u00A0:.+?Nom du compte\\u00A0:\s*(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Domaine du compte\\u00A0:""",
    """exa_regex=Raison de l\\u2019\\u00E9chec\\u00A0:\s*({failure_reason}.+?)\s*\\u00C9tat\\u00A0:""",
    """exa_regex=Sujet.+?Nom du compte\\u00A0:\s*(?=\w)({src_user}.+?)\s*Domaine du compte\\u00A0:""",
    """exa_regex=Sujet.+?Domaine du compte\\u00A0:\s*(?=\w)({src_domain}[^:]+?)\\s*ID d\\u2019ouverture de session\\u00A0:""",
    """exa_regex=\s*Sous-\\u00E9tat\\u00A0:\s*({result_code}.+?)\s*Informations sur le processus\\u00A0:"""
    ]
    DupFields = [
      "result_code->failure_code"
    ]

wazuh-windows-template = {
    Vendor = Wazuh
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """exa_json_path=$.['data.id'],exa_field_name=event_code""",
      """exa_json_path=$.@timestamp,exa_field_name=time""",
      """exa_json_path=$.['data.dstuser'],exa_field_name=dest_user,exa_match_expr=!Contains($.['data.dstuser'],"(no user)")""",
      """exa_json_path=$.['data.status'],exa_field_name=result""",
      """exa_json_path=$.location,exa_field_name=log_location""",
      """exa_json_path=$.['data.data'],exa_field_name=data""",
      """exa_json_path=$.path,exa_field_name=log_path""",
      """exa_json_path=$.['agent.id'],exa_field_name=agent_id""",
      """exa_json_path=$.['manager.name'],exa_field_name=wazuh_manager""",
      """exa_json_path=$.['rule.description'],exa_field_name=description""",
      """exa_json_path=$.['decoder.name'],exa_field_name=decoder_name"""
    
}
```