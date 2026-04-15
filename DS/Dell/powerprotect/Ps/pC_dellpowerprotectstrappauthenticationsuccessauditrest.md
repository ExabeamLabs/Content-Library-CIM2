#### Parser Content
```Java
{
Name = "dell-powerprotect-str-app-authentication-success-auditrest"
      ParserVersion = "v1.0.0"
      Conditions = [ """sms: """,""";id=""", """;desc=""", """;app=""", """AUDIT-REST""" ]

powerprotect-str-auditevents}{
      Name = "dell-powerprotect-str-app-authentication-success-auditrest"
      ParserVersion = "v1.0.0"
      Conditions = [ """sms: """,""";id=""", """;desc=""", """;app=""", """AUDIT-REST""" powerprotect-str-auditevents ={
      Vendor = "Dell"
      Product = "PowerProtect"
      TimeFormat = "epoch_sec"
      Fields = [
          """\s({host}[\w.-]+)\ssms:\s\{epoch=({time}\d{10});""",
          """id='({event_id}[^']+)';""",
          """desc='({operation}[^']+)';""",
          """level=({severity}\d);""",
          """user='({user}[\w\.\-\!\#\^\~]{1,40}\$?);'""",
          """role='({role}[^']+)';""",
          """app='({app}[^']+)';""",
          """client_ip='({src_ip}(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?))';""",
          """src='\{scheme=\d;host='({src_host}[\w.-]+)';location='({src_file_path}({src_file_dir}[^']*\/)?(({src_file_name}[^'.]*)?(\.({src_file_ext}[^\\\/\']+))?))';""",
          """dest='\{scheme=\d;host='({dest_host}[\w.-]+)';location='({file_path}({file_dir}[^']*\/)?(({file_name}[^'.]+)?(\.({file_ext}[^\\\/\']+))?))';""",
          """;result='({result}[^']+)';""",
          """method='({method}[^']+)';""",
          """uri='({uri}[^']+)';""",
          """http_status_code=({http_response_code}\d+);""",
          """err_msg='({error_info}[^']+)';""",
          """err_num=({error_code}\d+);""",
          """product='({object_name}[^']+)';"""
    ]
}
}


#============================================== Start of DefaultParsersAA section ==================================================================
DefaultParsersAA = [

{
Name = "appsense-am-leef-alert-trigger-success-warning"
Vendor = "AppSense"
Product = "AppSense Application Manager"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a"]
Conditions = [
"""AppSense Application Manager"""
"""SourceName="""
"""Message="""
"""EventCode="""
]
Fields = [
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""ComputerName=({host}({dest_host}[^\s]+))"""
"""Sid=({dest_user_sid}[^\s]+)"""
"""\s+Type=({alert_severity}[^\s]+)"""
"""\'\w+:\\+users\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Hash:(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"""
"""Vendor:\s+({process_vendor}[^\]]+)"""
"""Message=AppSense Application Manager ({alert_type}({alert_name}.+?))\s+(of [^\w]|\'|for)"""
"""Message=(The file )?\'.+?\'( has had)?\s+({alert_type}({alert_name}.+?))\s*(\.|of|for)"""
"""Message=\'(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\'"""
"""\'({path}({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?)))(\s+\[\w+:|')"""
]
ParserVersion = "v1.0.0"
}


{
  Name = openvpn-ov-json-vpn-login-success-connection
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "MMM dd HH:mm:ss"]
  Conditions = [ 
""" openvpn[""" 
"""MULTI_sva: pool returned """
"""IPv4=""" 
]
  Fields = [
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """ openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """hostname":"({host}[^"]+)""",
    """exa_json_path=$.@timestamp,exa_field_name=time""",
    """exa_regex= openvpn\[\d+\]:\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})):({src_port}\d+)""",
    """exa_regex=IPv4=({src_translated_ip}[A-Fa-f:\d.]+)""",
    """exa_json_path=$.beat.hostname,exa_field_name=host"""
  ]
},

{
  Name = openvpn-ov-str-vpn-logout-success-reset
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
"""Connection reset, restarting"""
"""openvpn""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d+)""",
    """(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\W?\d+\s\d+:\d+:\d+\s\d+\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\/({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({src_port}\d+)""",
    """({additional_info}Connection reset, restarting)"""
  ]
},

{
  Name = openvpn-ov-str-vpn-logout-success-reset-1
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
"""[soft,connection-reset]"""
"""client-instance restarting"""
"""openvpn""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d+)""",
    """(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\s\W?\d+\s\d+:\d+:\d+\s\d+\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\/({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({src_port}\d+)""",
    """\[soft,connection-reset\]\s*({result}[^,]+)""",
    """({additional_info}client-instance restarting)"""
  ]
},

{
  Name = openvpn-ov-str-vpn-logout-success-timeout
  ParserVersion = v1.0.0
  Vendor = Open VPN
  Product = Open VPN
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""openvpn"""
"""Inactivity timeout""" 
]
  Fields = [
    """openvpn\[({process_id}[^\]]+)\]""",
    """openvpn\[[^\]]+\]\:\s(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\/({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\:({src_port}\d+)""",
    """({event_name}Inactivity timeout)""",
    """Inactivity timeout\s({additional_info}[^\"]+?)\s*("|$)"""
  ]
},

{
  Name = mimecast-seg-cef-email-send-receive-rcpt
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""acc":""""
""""MsgId":"""
""""aCode":"""" 
""""Dir":""""
""""Sender":""""
""""Rcpt":"""",
""""Delivered":"""
]
  Fields = [
    """"acc":"({host}[^",]+)"""",
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Act":"({action}[^"]+)""",
    """request=({result}\S+)\s""",
    """"Rcpt":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """"Subject":"(|({email_subject}[^"]+?))\s*"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Sender":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"headerFrom":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"SpamScore":\s*"?({spam_score}\d+)"""
    """"MsgId":"<({message_id}[^"]+?)>""""
    """"Virus":"({alert_name}[^"]+)""""
    """"Err":"({failure_reason}[^"]+)""""
    """"AttCnt":\s*"?({attachment_count}\d+)""",
  ]
},
{
  Name = mimecast-seg-cef-email-send-receive-rcpt-2
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""acc":""""
""""MsgId":"""
""""aCode":"""" 
""""Dir":""""
""""Sender":""""
""""Rcpt":""""
]
  Fields = [
    """"acc":"({host}[^",]+)"""",
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Act":"({action}[^"]+)""",
    """request=({result}\S+)\s""",
    """"Rcpt":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """"Subject":"(|({email_subject}[^"]+?))\s*"""",
    """"Dir":"({direction}[^"]+?)"""",
    """"IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"Sender":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"headerFrom":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"SpamScore":\s*"?({spam_score}\d+)"""
    """"MsgId":"<({message_id}[^"]+?)>""""
    """"Virus":"({alert_name}[^"]+)""""
    """"Err":"({failure_reason}[^"]+)""""
    """"AttCnt":\s*"?({attachment_count}\d+)""",
  ]
},
{
  Name = mimecast-seg-cef-email-send-receive-attname
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
  Conditions = [ 
""""acc":""""
""""MsgId":""""
""""AttCnt":"""
""""AttNames":""" 
""""aCode":"""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w.\-]+ """,
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"AttNames":\[({email_attachments}[^\]]+)\]""",
    """"aCode":"(|({alert_id}[^"]+?))"""",
    """"MsgSize":"*({bytes}\d+)""",
    """"Subject":"({email_subject}[^"]+?)\s*"""",
    """"Sender":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """"datetime":"({time}\d+-\d+-\d+T\d+:\d+:\d+-\d+)""",
    """"AttCnt":\s*"?({attachment_count}\d+)""",
    """"AttSize":\s*({attachment_size}\d+)""",
    """"Hld":"({result}[^"]+)""",
    """"MsgId":"<\\*"?({message_id}[^,]+)>"""",
    """"AttNames":\[["\\]+({email_attachment}[^"]+\.({file_ext}[^"]+?))["\\]+"""
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Act\\?":"({action}[^"]+)""""
  ]
},

{
  Name = postfix-postfix-mix-email-sent
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
"""postfix"""
"""dsn=2."""
"""status=sent""" 
]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """\Wrt=({time}\d{13})""",
    """({message_id}[^\s"]+): to=<""",
    """"host(_name)?":"({host}[^"]+)""",
    """\d\d:\d\d:\d\d ({host}\S+) ( postfix[^:]+: )?""",
    """\Wto=<?(\\u\d+)?((({dest_user}[\w\-\.]+)@localhost)|(({=dest_user}[^@>]+?)@({dest_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|>]+)))""",
    """\Wrelay=({dest_host}[\w\-.]+)\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """originalAgentHostName=({host}[^"]+)\soriginalAgentAddress"""
    """\Wstatus=({result}\w+)"""
    """Hostname=({host}[\w\-.]+)""",
    """\s({bytes}\d+)\s+bytes in """
  ]
},

{
  Name = postfix-postfix-kv-email-queue
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""postfix"""
"""from=<"""
"""nrcpt=""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)"""
    """({host}[\w.\-]+) postfix""",
    """({message_id}[^\s"]+): from=<""",
    """\Wfrom=<?(\\u\d+)?((({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_host}[^@\>\.]+)\.(?:localdomain|local|company\.web\.ds))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+)))""",
    """\ssize=({bytes}\d+)""",
    """\snrcpt=({num_recipients}\d+)""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"host(_name)?":"({host}[^"]+)"""
    """\Wto=<({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]
},

{
  Name = postfix-postfix-str-email-subject
  ParserVersion = v1.0.0
  Vendor = Postfix
  Product = Postfix
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss" ]
  Conditions = [ 
"""postfix"""
"""header Subject:""" 
]
  Fields = [
    """\s*({time}\w+\s*\d?\d\s\d+:\d+:\d+)""",
    """\d\d:\d\d:\d\d ({host}\S+) postfix[^:]+:\s*({message_id}[^\s:]+)""",
    """\WSubject:\s*({email_subject}[^;]+)""",
    """\Wfrom=<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))""",
    """\Wto=<({email_recipients}[^\>]+)""",
    """\Wto=<({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))""",
    """\Wfrom (unknown|({src_host}[\w\-.]+))\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
},

{
  Name = mimecast-seg-cef-email-url
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""fromUserEmailAddress":""" 
""""userEmailAddress":""""
""""ttpDefinition":""""
""""url":""""
""""scanResult":""""
""""subject"""" 
]
  Fields = [
    """"date":"({time}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"category":"(Unknown|({category}[^"]+))""",
    """"+fromUserEmailAddress"+:"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"+userEmailAddress"+:"+({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"+url"+:"+({url}[^"]+)""",
    """"+ttpDefinition"+:"+({service_name}[^"]+)""",
    """"+subject"+:"+\s*({email_subject}.+?)\s*"+""",
    """"+route"+:"+({direction}[^"]+)""",
    """"+scanResult"+:"+({result}[^"]+)""",
    """"+scanResult"+:"+(clean|({failure_reason}[^"]+))""",
    """"sendingIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"(messageId|MsgId)":"<({message_id}[^"]+)>"""",
    """"creationMethod"+:"+({operation}[^",]+)"""
    ]
},

{
  Name = mimecast-seg-cef-email-inbound
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""aCode":""""
""""acc":""""
""""Route":"In"""
""""MsgId":""""
""""Subject":"""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) ([\w.\-]+) """,
    """"datetime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d+)"""",
    """"Route":"({direction}[^"]+)""",
    """"(?:id|aCode)":"({alert_id}[^"]+)""",
    """"(recipientAddress|Recipient)":"({email_user}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""",
    """(senderAddress|Sender)":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))""",
    """headerFrom":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))""",
    """"SenderDomain":"({email_domain}[^"]+)"""",
    """"Subject":"({email_subject}[^"]+?)\s*"""",
    """"(messageId|MsgId)":"<({message_id}[^"]+)>"""",
    """"(?:action|actions)":"({action}[^"]+)""",
    """"actionTriggered":"({action}[^"]+)""",
    """"(Source)?IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"fileName":"({email_attachment}[^"]+)"""",
    """"Size":({bytes}\d+)""",
    """"Virus":"({alert_name}[^"]+)""""
    """"UrlCategory":"({category}[^"]+)"""
  ]
},

{
  Name = delinea-centrifyis-kv-process-create-success-suite
  ParserVersion = v1.0.0
  Vendor = Delinea
  Product = Centrify Infrastructure Services
  TimeFormat = "epoch_sec"
  Conditions = [ 
"""AUDIT_TRAIL|Centrify Suite"""
"""dzdo command execution ends"""
]
  Fields = [
    """utc=({time}\d{10})""",
    """\d+\|\d+\|({event_name}.+?)\|\d""",
    """pid=({process_id}\d+)""",
    """command=({process_path}({process_dir}.*?)(\/+({process_name}[^\/]+?))?)\s*(\w+=|$)"""
    """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """status=({result}.+?)\s\w+=""",
    """parameters=({process_command_line}.+?)$"""
  ]
},

{
    Name = mimecast-seg-sk4-email-receive-impersonationprotect
    Vendor = Mimecast
    Product = Mimecast Secure Email Gateway
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"impersonationResults":""", """"impersonationDomainSource":""", """"senderAddress":""", """"recipientAddress":""" ]
    Fields = [
      """"eventTime":\s*"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}(\+|-)\d+?)"""",
      """"senderAddress":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
      """"recipientAddress":\s*"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """"senderIpAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"subject":\s*"({email_subject}[^"]+?)"""",
      """"action":\s*"({action}[^"]+?)"""",
      """"messageId":\s*"<({message_id}[^",]+?)>"""",
      """"definition":\s*"({additional_info}[^",]+?)"""",

    ]
	ParserVersion = "v1.0.0"
},

{
  Name = mimecast-seg-cef-email-hold
  ParserVersion = v1.0.0
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
""""recipientAddress":""""
""""senderAddress":""""
""""fileType":""""
""""result":""""
""""route":""""
]
  Fields = [
    """"date":"({time}\d+-\d+-\d+T\d+:\d+:\d+\+\d+)""",
    """dproc=({dproc}[^=]+?)\s+\w+=""",
    """"senderIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"Route":"({direction}[^"]+)""",
    """"(?:id|aCode)":"({alert_id}[^"]+)""",
    """"(recipientAddress|Recipient)":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """(senderAddress|Sender)":"(<>|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)(?<!prd)(?<!localdomain))"""",
    """"Subject":"({email_subject}[^"]+?)\s*"""",
    """"(messageId|MsgId)":"({message_id}[^"]+)""",
    """"fileName":"({file_name}({email_attachment}[^"]+\.({file_ext}[^"]+)))""",
    """"fileType":"({file_type}[^"]+)""",
    """"fileHash":"({file_hash}[^"]+)""",
    """"(?:action|actions)":"({action}[^"]+)""",
    """"actionTriggered":"(none|({action}[^"]+))""",
    """"SourceIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"result":"({result}[^"]+)""",
    """"subject":"({email_subject}[^"]+)"""
    """"UrlCategory":"({category}[^"]+)"""
  ]
},


{
  Name = skysea-cv-csv-email-send-success
  ParserVersion = v1.0.0
  Vendor = SkySea
  Product = SkySea ClientView
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ 
""",メール,""" 
]
  Fields = [
    """({host}[\w\-.]+),\d+,({src_host}[\w\-.]+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,[^,]*,({user}[\w\.\-\!\#\^\~]{1,40}\$?),(|({full_name}[^,\(\（]+(\（[^\）,]+\）)?)[^,]*),({time}\d+\/\d+\/\d+ \d+:\d+:\d+),([^,]*,){4}\s*(|({email_subject}[^,]+?))\s*,([^,]*,){21}(({email_recipients}<?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))[^,]*)|[^,]*),(<?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+))>?|[^,]*),\s*(|({email_attachments}[^,]+?\.({file_ext}[^,]+)))\s*,"""
  ]
},

{
  Name = cloudflare-waf-cef-http-session-clientip
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
""""edgeResponseStatus":"""
""""clientIP":""""
""""source":"""" 
""""clientRequestHTTPMethodName":"""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s+[^\s]+\s+""",
    """"ClientDeviceType":"({device_type}[^"]+)""",
    """"clientCountryName":"({src_country}[^"]+)""",
    """"clientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"edgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))""",
    """"originResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"clientRequestHTTPMethodName":"({method}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"ClientRequestReferer":"({referrer}[^"]+?)",""",
    """"clientRequestHTTPHost":"({web_domain}[^"<,]+)""",
    """"clientRequestPath":"({uri_path}[^"]+)""",
    """"clientRequestHTTPProtocol":"({protocol}[^"\/]+)""",
    ]
},

{
  Name = akamai-ca-json-http-session-webactivity
  ParserVersion = v1.0.0
  Vendor = Akamai
  Product = Cloud Akamai
  TimeFormat = "epoch_sec"
  Conditions = [ 
""""reqPort":""""
""""reqHost":""""
""""status"""
""""reqPath":"""" 
]
ExtractionType = json
  Fields = [
    """exa_json_path=$.start,exa_regex=({time}\d{10})""",
    """exa_json_path=$..proto,exa_field_name=protocol""",
    """exa_json_path=$..status,exa_field_name=http_response_code""",
    """exa_json_path=$..reqTimeSec,exa_regex=({time}\d{10})""",
    """exa_json_path=$..statusCode,exa_field_name=http_response_code""",
    """exa_json_path=$..queryStr,exa_field_name=query_string,exa_match_expr=!InList($.queryStr,"")""",
    """exa_json_path=$..UA,exa_field_name=user_agent,exa_match_expr=!InList($.UA,"")""",
    """exa_json_path=$..cliIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..reqPort,exa_field_name=dest_port""",
    """exa_json_path=$..reqHost,exa_field_name=web_domain""",
    """exa_json_path=$..reqMethod,exa_field_name=method""",
    """exa_json_path=$..reqPath,exa_field_name=uri_path""",
    """exa_json_path=$..reqQuery,exa_field_name=uri_query""",
    """exa_json_path=$..edgeIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$..bytes,exa_field_name=bytes""",
  ]
},

{
  Name = squid-s-json-http-session-responsestatus
  ParserVersion = v1.0.0
  Vendor = Squid
  Product = Squid
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
"""http_method"""
"""http_status_code"""
"""squid_request_status"""
]
  Fields = [
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """http_username":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """http_method":"({method}[^"]+)"""",
    """squid_request_status":"({proxy_action}[^"]+)"""",
    """http_url":"(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({url}(({protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?({uri_path}\/[^\s\?"]*)?({uri_query}\?[^"\s]*)?))""",
    """http_status_code"*:({http_response_code}\d+)""",
    """ip_server":"(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """ip_client":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """http_reply_size":({bytes_out}\d+)""",
    """http_received_size":({bytes_in}\d+)""",
    """http_mime_type":"(-|({mime}[^"]+?))","""
  ]
},

{
  Name = forcepoint-wsg-kv-http-session-action
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Websense Security Gateway
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
"""vendor=Websense"""
"""http_user_agent="""
"""http_proxy_status_code=""" 
]
  Fields = [
    """({host}\S+)\s+vendor=""",
    """\sdst_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc_host=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssrc_port=({src_port}\d+)""",
    """\sdst_port=({dest_port}\d+)""",
    """user=[^=]+?({user_ou}\w+=[^\/]+?DC=\w+\/({full_name}[^\(]+?))\s+(\([^\)]+\)\s+)?src_host=""",
    """\saction=({action}[^\s]+)""",
    """\shttp_method=(-|({method}[^\s]+))""",
    """\sbytes_in=({bytes_in}\d+)""",
    """\sbytes_out=({bytes_out}\d+)""",
    """\surl=(?:-|({url}[^\s"]+))""",
    """\surl=(?:-|({protocol}[^:\s]+)):""",
    """\surl=([^:]+:\/+)?({web_domain}[^\s\/:]+)[^"]*?$""",
    """\surl=(?:-|\w+:\/+[^\s\/]+)\/+({uri_path}[^?\s]*)""",
    """\surl=(?:-|(?=(?)(?:[^?]+\?({uri_query}[^\s"]+))))""",
    """\shttp_user_agent=(?:-|({user_agent}[^=]+?))\s+http_proxy""",
    """\scategory=({category_id}\d+)\s+user""",
    """\shttp_content_type=(?:-|({mime}[^"]+?))\s+http_""",
    """\shttp_proxy_status_code=({http_response_code}\d+)""",
    """\sdisposition=({disposition}[^=]+?)\s+(\w+=|$)""",
    """\sreason=(-|({result_reason}[^=]+?))\s+(\w+=|$)"""
  ]
},

{
  Name = forcepoint-wsg-cef-http-session-request
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Websense Security Gateway
  TimeFormat = ["epoch", "epoch_sec"]
  Conditions = [ 
"""CEF"""
"""|Forcepoint|"""
""" app=""" 
""" request=""" 
]
  Fields = [
    """\srt=({time}\d{10,13})""",
    """\sdvc=(-|({host}[^\s]+))""",
    """\sdvchost=({host}[^\s]+)""",
    """\sshost=({src_host}[^\s]+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sspt=({src_port}\d+)""",
    """\sdpt=({dest_port}\d+)""",
    """\ssuser=(-|(?:\w+:\/+[^=]+)\s+({user_ou}[^\/]+)\/({full_name}[^=]+?))\s+\w+=""",
    """\sact=({action}[^=]+?)\s\w+=""",
    """\srequestMethod=(?:-|({method}[^=]+?))\s\w+=""",
    """\sin=({bytes_in}\d+)""",
    """\sout=({bytes_out}\d+)""",
    """\sapp=(?:-|({protocol}[^=]+?))\s\w+=""",
    """\srequestProtocol=(?:-|({protocol}[^=]+?))\s\w+=""",
    """\sdhost=(?:|({web_domain}[^=]+?))\s\w+=""",
    """\srequest=({url}\S+)""",
    """\srequest=(?:-|(\w+:\/+[^\/]+({uri_path}\/[^\s\?]+)({uri_query}\?[^\s]+)?))(\s+\w+=|$)""",
    """\srequestUrlFileName=(?:|({uri_path}[^=]+?))\s\w+=""",
    """\srequestUrlQuery=(?:|({uri_query}[^=]+?))\s\w+=""",
    """\srequestClientApplication=(?:-|({user_agent}[^=]+?))\s+(\w+=|$)""",
    """CEF:([^\|]+\|){4}(\d+|({category}[^\|]+))\|""",
    """CEF:([^\|]+\|){4}(|({category_id}\d+))\|""",
    """\scs4=({category}[^=]+?)(\s+\w+=|;)""",
    """\scs5=({sub_category}[^=]+?)(\s+\w+=|;)""",
    """\sflexString1=(?:User Defined[^=]+?|({category}[^=]+?))\s+\w+=""",
    """\sflexString2=(?:User Defined.+?|({sub_category}.+?))\s+\w+=""",
    """\scs3=(?:-|({mime}[^=]+?))(\s+\w+=|;)""",
    """suser=(-|({last_name}[^,]+),\s({first_name}([A-Za-z]+){1}(\s\w){0,1}))\s""",
    """suser=\w+:\/+([^\s]+)?\s*((CN|OU)\\+=[^,]+,){1,2}DC\\=[^,]+,DC\\=[^\/]+\/({full_name}({last_name}[^\\]+)\\+,\s*({first_name}[^=]*?))\s\w+=""",
    """loginID=(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]
},

{
  Name = forcepoint-ngfw-cef-network-session-fail-discarded
  Vendor = Forcepoint
  Product = Forcepoint Next-Gen Firewall
  ParserVersion = v1.0.0
  TimeFormat = ["epoch","MMM dd yyyy HH:mm:ss"]
  Conditions = [ 
"""CEF:"""
"""|FORCEPOINT|"""
"""|Connection_Discarded|""" 
]
  Fields = [
    """ahost=\s*({host}.+?)(\s\w+=)""",
    """\Wrt=({time}\d{13})""",
    """src=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """dhost=\s*({dest_host}.+?)(\s\w+=)""",
    """dst=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(\s\w+=)""",
    """amac=\s*({src_mac}.+?)(\s\w+=)""",
    """dvc=\s*(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s|({src_host}[\w\.\-]+))""",
    """app=\s*({protocol}.+?)(\s\w+=)""",
    """\Win=({bytes_in}\d+)""",
    """\Wout=({bytes_out}\d+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\sdeviceInboundInterface=({src_interface}.+?)\s*\w+=""",
    """\sdeviceOutboundInterface=({dest_interface}.+?)\s*\w+=""",
    """proto=\s*({protocol}.+?)(\s\w+=)"""
    """({operation}Connection_Discarded)"""
    """\Wrt=({time}\w\w\w \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  ]
},

{
  Name = forescout-counteract-str-network-traffic-success-established
  Vendor = Forescout
  Product = Forescout CounterACT
  ParserVersion = v1.0.0
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ 
"""Connection has been established:""" 
]
  Fields = [
    """(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s""",
    """({time}\w+\s+\d+ \d+:\d+:\d+)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """from\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+to\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]""",
    """({event_name}Connection has been established)"""
  ]
},

{
  Name = "forescout-counteract-kv-network-traffic-status"
  ParserVersion = "v1.0.0"
  Vendor = "Forescout"
  Product = "Forescout CounterACT"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""]: Log: Connection Status. Details: """
""" Connection Status: """
"""Vendor:"""
  ]
  Fields = [
"""(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s"""
"""Connection Status:\s+({action}({result}[^\s]+).+?)\.\s+Type"""
"""Source:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
},

{
Name = "arbor-a-str-network-traffic-fail-block"
Vendor = "Arbor"
Product = "Arbor Cloud"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
"""arbor-networks-aps:"""
"""Blocked Host"""
]
Fields = [
  """\d\d:\d\d:\d\d\s({host}[^\s]*)\s""",
  """Blocked\shost\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sby\s({failure_reason}.+)\susing""",
  """\susing\s({protocol}[^\/]*)\/\d+\s"""
  """destination\s({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s""",
  """\ssource\sport\s({src_port}\d+)"""
  """\w+\/({dest_port}\d+)\s\("""
  """\/\d+\s\(({operation}[^\)]*)""",
  """arbor-networks-aps:\s*({action}[^:]*):\s"""
]
ParserVersion = "v1.0.0"
},

{
Name = "infoblox-bddi-cef-alert-trigger-success-alert"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Infoblox|"""
""" act="ALERT"""
]
Fields = [
"""CEF:([^\|]*\|){4}({rule_id}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s"""
"""act="({action}[^"]+)"""
"""cat="({alert_type}({operation}[^"]+))"""
"""spt=({src_port}\d+)"""
"""dpt=({dest_port}\d+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""fqdn=((na\s)|({dns_query}[\w\-.]+))"""
"""fqdn=(NA|({web_domain}[^\s]+))\s*"""
]
ParserVersion = "v1.0.0"
}

{
Name = "infoblox-bddi-cef-network-traffic-threat"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""CEF:"""
"""|Infoblox|"""
""" act=""""
]
Fields = [
  """CEF:([^\|]*\|){4}({rule_id}[^\|]+)\|({alert_name}[^\|]+)\|({alert_severity}[^\|]+)""",
  """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s""",
  """act="({action}[^"]+)""",
  """cat="({alert_type}[^"]+)""",
  """spt=({src_port}\d+)""",
  """dpt=({dest_port}\d+)""",
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """fqdn=(NA|({dns_query}[\w\-.]+))""",
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Fields = [
  """"_system_name":"({host}[\w\-.]+)"""",
  """"ts"+:({time}\d+)""",
  """"uid\\?"+:\\?"+({connection_id}[^"\\]+)""",
  """"id\.orig_h\\?"+:\\?"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"id\.orig_p\\?"+:({src_port}\d+)""",
  """"id\.resp_h\\?"+:\\?"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"id\.resp_p\\?"+:({dest_port}\d+)""",
  """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
  """"proto":"({protocol}[^"]+)""""
]
Name = "zeek-z-json-network-traffic-success-dpd"
Conditions = [
""""_path":"dpd"""
""""id.orig_h":""""
""""uid":""""
""""id.resp_p":"""
]
ParserVersion = "v1.0.0"
},
{
Name = netwrix-auditor-kv-database-who
ParserVersion = "v1.0.0"
Vendor = Netwrix
Product = Netwrix Auditor
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""DataSource : SQL"""
"""Where :"""
"""Who :"""
]
Fields = [
"""When : ({time}[^\s]+)"""
"""What\s*:\s*(.+?\\+)?({db_name}[^\s]+)""",
"""Who\s*:\s*(({domain}[^\s]+)\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Where\s*:\s*({dest_host}[\w\-.]+)"""
"""Workstation\s*:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Details\s*:"""
"""ObjectType\s*:\s*({additional_info}.+?)\s*\w+\s*:\s*"""
"""Device name:\s*\"*({service_name}[^\",\s]+)"""
"""Message\s*:\s*({result_reason}.+?)\s*\w+\s*:"""
"""DataSource\s*:\s*({app}.+?)\s*\w+\s*:"""
"""Application name:\s*({app}.+?)\s*$"""
]
},

{
Name = "extrahop-revealx-json-dns-request-success-dnsquery"
Vendor = "Extrahop"
Product = "Extrahop Reveal(x)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""opcode":"QUERY"""
"""vendor":"ExtraHop"""
"""qname"""
"""qtype"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+-\d+:\d+)\s*({host}[^\s]+)""",
  """"proto":"({protocol}[^"]+)""",
  """"clientAddr":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"serverAddr":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """"clientPort":({src_port}\d+)""",
  """"serverPort":({dest_port}\d+)""",
  """"qname":"({dns_query}[^"]+)""",
  """"qtype":"({dns_query_type}[^"]+)""",
  """"error":"({error_code}[^"]+)""",
  """"rspBytes":({bytes}\d+)"""
]
ParserVersion = "v1.0.0"
},
{
Name = "crowdstrike-falcon-mix-dns-request-success-dnsrequest"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = ["epoch_sec", "epoch"]
ExtractionType = json
Conditions = [
""""event_simpleName":"""
""""DnsRequest""""
""""RequestType":"""
]
Fields = [
  """"OciContainerId"\s*:\s*"({container_id}[^"]+)"""",
  """"ComputerName":"({host}[\w\-\.]+)""""
  """"hostname":"({host}[\w\-.]+)"""",
  """"timestamp":\s*"({time}\d{10})""",
  """"DomainName":\s*"({dns_query}[^\"]+?)\s*"""",
  """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"LocalAddressIP6":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"RemoteAddressIP6":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"RemoteAddressIP4":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"LocalPort":\s*"({src_port}\d+)""",
  """"RemotePort":\s*"({dest_port}\d+)""",
  """"aid":\s*"({aid}[^\"]+)"""",
  """"aip":\s*"({aip}[a-fA-F:\d.]+)""",
  """"event_simpleName":\s*"({event_code}[^\"]+)"""",
  """"event_platform":"({os}[^"]+)"""",
  """src-account-name":"({account_name}[^"]+)""",
  """"IP4Records":"({dns_response}[^"]+)"""",
  """"ContextProcessId":"({process_guid}[^"]+)"""",
  """"FirstIP4Record":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
  """"RespondingDnsServer":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"QueryStatus":"({dns_query_flags}[^"]+)"""",
  """"RequestType":"({dns_query_type}[^"]+)""""
  """"ContextBaseFileName":"({file_name}[^"]+)""""
  """"name":\s*"({event_name}[^"]+)"""
  """exa_json_path=$.OciContainerId,exa_field_name=container_id"""
  """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
  """exa_json_path=$.hostname,exa_regex=({host}[\w\-.]+)"""
  """exa_json_path=$.timestamp,exa_field_name=time"""
  """exa_json_path=$.DomainName,exa_regex=({dns_query}[^\"]+?)\s*"""
  """exa_regex="DomainName":\s*"({dns_query}[^\"]+?)\s*"""",
  """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.LocalAddressIP6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.RemoteAddressIP6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """exa_json_path=$.RemoteAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.LocalPort,exa_field_name=src_port"""
  """exa_json_path=$.RemotePort,exa_field_name=dest_port"""
  """exa_json_path=$.aid,exa_field_name=aid"""
  """exa_json_path=$.aip,exa_regex=({aip}[a-fA-F:\d.]+)""",
  """exa_json_path=$.event_simpleName,exa_field_name=event_code"""
  """exa_json_path=$.event_platform,exa_field_name=os"""
  """exa_json_path=$.src-account-name,exa_field_name=account_name"""
  """exa_json_path=$.IP4Records,exa_field_name=dns_response"""
  """exa_json_path=$.ContextProcessId,exa_field_name=process_guid"""
  """exa_json_path=$.FirstIP4Record,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
  """exa_json_path=$.RespondingDnsServer,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """exa_json_path=$.QueryStatus,exa_field_name=dns_query_flags"""
  """exa_json_path=$.RequestType,exa_field_name=dns_query_type"""
  """exa_json_path=$.ContextBaseFileName,exa_field_name=file_name"""
  """exa_json_path=$.name,exa_field_name=event_name"""
  """exa_json_path=$.UserName,exa_regex=(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
]
ParserVersion = "v1.0.0"
},
{
Name = "infoblox-bddi-cef-dns-response-success-dns"
Vendor = "Infoblox"
Product = "BloxOne DDI"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""|Infoblox|"""
"""app=DNS"""
"""InfobloxDNSView="""
"""InfobloxDNSQType="""
]
Fields = [
     """src=(\s|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
     """dst=(\s|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
     """spt=(\s|({src_port}\d+))""",
     """proto=(\s|({protocol}[^\s]+))""",
     """app=({app}[^\s]+)""",
     """InfobloxDNSRCode=({dns_response_code}[^\s]+)\s""",
     """InfobloxDNSQType=(\s|({dns_query_type}[^\s]+))""",
     """destinationDnsDomain=(\s|({dns_query}[^\s]+))""",
     """msg=(\s|({additional_info}.+?));\s\.\s32768""",

]
ParserVersion = "v1.0.0"
},

{
Name = unix-unixnamed-str-dns-request-success-client-1
Vendor = Unix
Product = Unix Named
TimeFormat = "dd-MMM-yyyy HH:mm:ss.SSS"
Conditions = [
  """ query: """
  """ info: client """
  """ named["""
  """queries:"""
]
Fields = [
  """({time}\d\d-\w+-\d\d\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """client\s*({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\#({src_port}\d+)"""
  """query:\s*({dns_query}[^\s]+)"""
  """query:\s*({dns_query}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sIN\s({dns_query_type}[^\s]+)\s+({dns_query_flags}[^"\s]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "zeek-z-json-dns-request-success-dns"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
ExtractionType = json
Conditions = [
""""id.orig_h":"""
""""id.resp_h":"""
""""dns","""
""""qtype_name":"""
]
Fields = [
  """"_system_name":"({host}[\w\-.]+)""",
  """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
  """"id\.orig_h":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """"id\.orig_p":({src_port}\d+)""",
  """"id\.resp_h":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """"id\.resp_p":({dest_port}\d+)""",
  """"proto":"({protocol}[^"]+)""",
  """"query":"({dns_query}[^"]+)"""",
  """"qtype_name":"({dns_query_type}[^"]+)""",

  """exa_json_path=$._system_name,exa_regex=^({host}[\w\-.]+)$""",
  """exa_json_path=$.ts,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
  """exa_json_path=$.['id.orig_h'],exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$""",
  """exa_json_path=$.['id.orig_p'],exa_field_name=src_port""",
  """exa_json_path=$.['id.resp_h'],exa_regex=^({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?$""",
  """exa_json_path=$.['id.resp_p'],exa_field_name=dest_port""",
  """exa_json_path=$.proto,exa_field_name=protocol""",
  """exa_json_path=$.query,exa_field_name=query""",
  """exa_json_path=$.qtype_name,exa_field_name=dns_query_type"""
]
ParserVersion = "v1.0.0"
},

{
  Name = "onelogin-o-cef-app-login-assumingactinguserid"
  ParserVersion = "v1.0.0"
  Vendor = "OneLogin"
  Product = "OneLogin"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """assuming_acting_user_id":""", """app_name":""", """user_name":""", """event_type_id":""", """destinationServiceName=OneLogin""" ]
  Fields = [
    """"created_at":\s*"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3}Z)""",
    """\WdestinationServiceName=({app}\w+)""",
    """"app_name":\s*"\s*({app}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"event_type_id":\s*({activity_id}\d+)""",
    """"actor_user_name":"({full_name}[^"]+?)\s*"""",
    """"ipaddr":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"notes":\s*"\s*({failure_reason}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"notes":\s*"\s*({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"custom_message":\s*"\s*({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"error_description":\s*"\s*({additional_info}([^\\"]|(\\\\)*\\"|\\\\)+?)\s*"""",
    """"event_type_name":"({operation}[^"]+)"""",
    """"event_type_description":"({additional_info}[^"]+)"""",
    """"user_id":({account}({user_id}\d+))""",
    """suser=(({account}({user_id}\d+))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
    """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  ]
},

{
  Name = "epic-siem-cef-app-login-success-login"
  ParserVersion = "v1.0.0"
  Vendor = "Epic"
  Product = "Epic SIEM"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Epic|Security-SIEM|""", """|LOGIN|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """({host}[\w\-.]+)\s+CEF:""",
    """LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """workstationID=({dest_host}[\w\-.]+)""",
    """shost=({src_host}[\w\-.]+)""",
    """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ROLE=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """USERJOB=(|({resource}.+?))\s+(\w+=|$)""",
  ]
},

{
  Name = "epic-siem-cef-app-login-fail-failedlogin"
  ParserVersion = "v1.0.0"
  Vendor = "Epic"
  Product = "Epic SIEM"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Epic|Security-SIEM|""", """|FAILEDLOGIN|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """({host}[\w\-.]+)\s+CEF:""",
    """LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """workstationID=({dest_host}[\w\-.]+)""",
    """shost=({src_host}[\w\-.]+)""",
    """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ROLE=({additional_info}.+?)\s+(\w+=|$)""",
    """USERJOB=({resource}.+?)\s+(\w+=|$)""",
    """LOGINERROR=({failure_reason}.+?)\s+(\w+=|$)""",
  ]
},

${mimecast-json-template.mimecast-json-event}{
  Name = "mimecast-seg-cef-app-login-fail-logonauthfailed"
  ParserVersion = "v1.0.0"
  Vendor = "Mimecast"
  Product = "Mimecast Secure Email Gateway"
  Conditions = [ """"auditType":"Logon Authentication Failed"""", """"category":""", """eventInfo":""", """"eventTime":""" ]
  Fields = ${mimecast-json-template.mimecast-json-event.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w.\-]+ """,
    """IP:\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),""",
    """"user":"(|({email_address}[^@]+@[^"]+?))"""",
    """\sReason:\s(|({failure_reason}[^=]+?))(\s+\w+=|\s*$)""",
    """\sApplication:\s*({app}[^,]+?),""",
    """"user":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """exa_regex=\sReason:\s*(|({failure_reason}[^="]+?))(\s+\w+:|\s*")""",
    """exa_regex=\sApplication:\s*({app}[^,]+?),""",    
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-delete-success-moveitdelfile"
  ParserVersion = v1.0.0
  Conditions = [ """AgentBrand: MOVEit""", """Delete File""" ]
  Fields = ${MoveITParsersTemplates.moveit-activity.Fields}[
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-delete-success-moveitdmzdelfile"
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Delete File""" ]
  Fields = ${MoveITParsersTemplates.moveit-activity.Fields} [
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
    """({operation}Delete)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-delete-success-moveitdmzdelfolder"
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Delete Folder""" ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+?(\.({file_ext}[^,]+))?),\s\w+:"""
    """\sFolderPath:\s*({file_path}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
    """({operation}Delete)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-download-success-moveitdownload"
  ParserVersion = v1.0.0
  Conditions = [ """AgentBrand: MOVEit""", """Download""" ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
  """\sFileID:\s*({file_id}[^,]+)"""
  """\sFileName:\s*({file_name}[^,]+\.({file_ext}[^,]+))"""
  """\sFolderPath:\s*({file_dir}[^,]+)"""
  """\sXFerSize:\s*({bytes}\d+)"""
  ]
},
${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-download-success-moveitdmzdownload"
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Download""" ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
    """({operation}Download)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-upload-success-moveitupload"
  ParserVersion = v1.0.0
  Conditions = [ """AgentBrand: MOVEit""", """Upload""" ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^,]+?(\.({file_ext}[^\s,\.]+))?),\s\w+:"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
    """({operation}Delete)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-upload-success-moveitdmzupload"
  ParserVersion = v1.0.0
  Conditions = [ """ MOVEitDMZ""", """ Upload """ ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
    """\sFileID:\s*({file_id}[^,]+)"""
    """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
    """\sFolderPath:\s*({file_dir}[^,]+)"""
    """\sXFerSize:\s*({bytes}\d+)"""
    """({operation}Upload)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-upload-success-moveitdmzsend"
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Send""" ]
  Fields =${MoveITParsersTemplates.moveit-activity.Fields} [
  """\sFileID:\s*({file_id}[^,]+)"""
  """\sFileName:\s*({file_name}[^.,]+\.({file_ext}[^,]+))"""
  """\sFolderPath:\s*({file_dir}[^,]+)"""
  """\sXFerSize:\s*({bytes}\d+)"""
  """({operation}Send)"""
  """TargetName:\s({full_name}[^,]+)"""
  """Parm2:\s({email_address}[^@]+@[^\.]+\.[^,]+)"""
  ]
},

${MoveITParsersTemplates.moveit-activity}{
  Name = "ipswitch-mdmz-kv-file-write-success-moveitdmzaddfolder"
  ParserVersion = v1.0.0
  Conditions = [ """MOVEitDMZ""", """Add Folder""" ]
},

{
Name = "netapp-n-xml-file-delete-success-4660"
Vendor = "NetApp"
Product = "NetApp"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4660</EventID>"""
  """SubjectUserSid"""
  """NetApp-Security-Auditing"""
]
Fields = [
  """<TimeCreated SystemTime="+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>"""
  """<EventID>({event_code}[^<]+)<\/EventID>"""
  """<EventName>({operation}({event_name}[^<]+))<\/EventName>"""
  """<Result>({result}[^<]+)</Result>"""
  """<Data Name\\*=('|")*SubjectIP("|')*.*?>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>"""
  """<Data Name\\*=('|")*SubjectUserSid('|")*>({user_sid}.+?)</Data>"""
  """<Data Name\\*=('|")*SubjectDomainName('|")*>({domain}.+?)</Data>"""
  """<Data Name\\*=('|")*SubjectUserName('|")*>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>"""
  """<Data Name\\*=('|")*ObjectServer('|")*>({object_server}.+?)</Data>"""
  """<Data Name\\*=('|")*ObjectType('|")*>({file_type}.+?)</Data>"""
  """<Data Name\\*=('|")*ObjectName('|")*>({file_path}.+?)<\/Data>"""
  """<Data Name\\*=('|")*ObjectName('|")*>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>"""
  """<Data Name\\*=('|")*ObjectName('|")*>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>"""
  """<Data Name\\*=('|")*ProcessName('|")*>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/"<]+?))</Data>"""
  """<Data Name\\*=('|")*(HandleID|HandleId)('|")*>({object_id}.+?)</Data>"""
]
ParserVersion = "v1.0.0"
},

{
Name = "netapp-n-xml-alert-trigger-success-4656"
Vendor = "NetApp"
Product = "NetApp"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """<EventID>4656</EventID>"""
  """SubjectUserSid"""
  """NetApp-Security-Auditing"""
]
Fields = [
  """<TimeCreated SystemTime="+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>([^<>]+?[\\\/]+)?({host}[^<>]+)<\/Computer>"""
  """<EventID>({event_code}[^<]+)<\/EventID>"""
  """<EventName>({alert_name}[^<]+)<\/EventName>"""
  """<Result>({result}[^<]+)<\/Result>"""
  """<Data Name\\*="*SubjectIP"*.*?>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data>"""
  """<Data Name\\*="*SubjectUserSid"*>({user_sid}[^<]+)<\/Data>"""
  """<Data Name\\*="*SubjectDomainName"*>({domain}.+?)<\/Data>"""
  """<Data Name\\*="*SubjectUserName"*>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>"""
  """<Data Name\\*="*ObjectServer"*>({object_server}.+?)<\/Data>"""
  """<Data Name\\*="*ObjectType"*>({alert_type}({object_class}.+?))<\/Data>"""
  """<Data Name\\*="*ObjectName"*>({file_path}.+?)<\/Data>"""
  """<Data Name\\*="*ObjectName"*>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>"""
  """<Data Name\\*="*ObjectName"*>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>"""
  """<Data Name\\*="*ProcessName"*>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/"<]+?))</Data>"""
  """<Data Name\\*="*(HandleID|HandleId)"*>({object_id}.+?)<\/Data>"""
  """<Data Name\\*="*DesiredAccess"*>\s*({access}.+?)\s*<\/Data>"""
]
ParserVersion = "v1.0.0"
},

{
   Name = "delinea-centrifyas-cef-endpoint-login-fail-pam"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""Centrify Suite""" 
"""|PAM|"""
"""denied|""" 
]
   Fields = [
"""utc=({time}\d{13})"""
"""\sahost=({host}[^=]+?)\s+\w+="""
"""\sclient=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(\(none\)|({src_host}[^=]+?)))\s+\w+=""",
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({service_name}[^=]+?)\s\w+=""",
"""reason=({failure_reason}[^=\|]+?)(\s+\w+=|\|)"""
   ]
},

{
   Name = "delinea-centrifyas-kv-endpoint-login-fail-trustedpath"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""|Centrify Suite|Trusted Path|"""
"""|Trusted path denied|""" 
]
   Fields = [
"""utc=({time}\d{13})"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\("""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\(\)\s@]+)\s+(\w+=|$)"""
"""\|({event_name}Trusted path\s+[^\|]*)\|"""
"""status=({result}.+?)\s+(\w+=|$)"""
"""pid=({process_id}\d+)"""
"""server=(({protocol}[^\\\/\s]+)[\\\/]+)?({dest_host}[\w\-.]+?)(@({dest_domain}[^\\\/\s]+))?\s+(\w+=|$)"""
"""reason=:?\s*({failure_reason}.+?)\s+(\w+=|$)"""
   ]
},
{
   Name = "delinea-centrifyas-kv-endpoint-login-success-trustedpath"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""|Centrify Suite|Trusted Path|"""
"""|Trusted path granted|""" 
]
   Fields = [
"""utc=({time}\d{13})"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\("""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\(\)\s@]+)\s+(\w+=|$)"""
"""\|({event_name}Trusted path\s+[^\|]*)\|"""
"""status=({result}.+?)\s+(\w+=|$)"""
"""pid=({process_id}\d+)"""
"""server=(({protocol}[^\\\/\s]+)[\\\/]+)?({dest_host}[\w\-.]+?)(@({dest_domain}[^\\\/\s]+))?\s*(\w+=|$|")"""
   ]
},

{
   Name = "delinea-centrifyas-kv-ssh-traffic-success-sshd"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""Centrify Suite|Centrify"""
"""SSHD granted""" 
]
   Fields = [
"""utc=({time}\d{13})"""
"""\sahost=({host}[^=]+?)\s+\w+="""
"""\sclient=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^=]+?))\s+\w+="""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({process_path}.+?)\s\w+="""
"""EntityName=(.+\\+)?({dest_host}[^\"\s]+)(\s|$)"""
"""\sauthMechanism=({auth}[^\s]{1,40})"""
   ]
},

{
   Name = "delinea-centrifyas-cef-endpoint-login-fail-sshd"
   ParserVersion = "v1.0.0"
   Vendor = "Delinea"
   Product = "Centrify Authentication Service"
   TimeFormat = "epoch"
   Conditions = [ 
"""Centrify Suite|Centrify"""
"""SSHD denied""" 
]
   Fields = [
"""utc=({time}\d{13})""",
"""\sahost=({host}[^=]+?)\s+\w+="""
"""\sclient=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^=]+?))\s+\w+="""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({process_path}.+?)\s\w+="""
"""EntityName=(.+\\+)?({dest_host}[^\"\s]+)(\s|$)"""
"""reason=({failure_reason}[^=\|]+?)(\s+\w+=|\|)"""
   ]
},

{
Name = "delinea-ss-cef-app-login-success-userlogin"
Vendor = "Delinea"
Product = "Secret Server"
TimeFormat = ["MMM dd yyyy HH:mm:ss","epoch_sec"]
Conditions = [
  """|Thycotic Software|Secret Server|"""
  """|USER - LOGIN|"""
  """ Item Name:"""
]
Fields = [
  """\d{2}:\d{2}:\d{2} ({host}[\w\-.]+) CEF:"""
  """\srt=({time}\d{10})"""
  """\srt=({time}\w+ \d{2} \d{4} \d{2}:\d{2}:\d{2})"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sduser=(({domain}[^\\=]+)[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
  """({app}Thycotic Software)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "delinea-ss-cef-app-login-fail-userloginfail"
Vendor = "Delinea"
Product = "Secret Server"
TimeFormat = ["MMM dd yyyy HH:mm:ss","epoch_sec"]
Conditions = [
  """|Thycotic Software|Secret Server|"""
  """|USER - LOGINFAILURE|"""
  """ Item Name:"""
]
Fields = [
  """\d{2}:\d{2}:\d{2} ({host}[\w\-.]+) CEF:"""
  """\srt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
  """\srt=({time}\d{10})"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sduser=(({domain}[^\\=]+)[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """Details:\s*({failure_reason}.+?)\s\w+="""
  """Details:\s*({additional_info}({failure_reason}[^:=]+?)(?:\sExpected:[^=]+?)?)\s+\w+=""",
  """({app}Thycotic Software)"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Ipswitch"
Product = "MoveIt Transfer"
TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
"""\s:\s+({operation}[^,]+),\s+ID:"""
"""\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sMessage:\s*({additional_info}.+?)\s*$"""
]
Name = "ipswitch-moveittransfer-kv-endpoint-login-success-signedon"
Conditions = [
"""MOVEitDMZ"""
"""Signed on"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Ipswitch"
Product = "MoveIt Transfer"
TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
"""\s:\s+({operation}[^,]+),\s+ID:"""
"""\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""TargetName:\s+(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)),"""
"""TargetID:\s+({dest_user_sid}[^,]+)"""
"""({operation}Add User)"""
"""\sID:\s({account_id}\d+)"""
]
Name = "ipswitch-moveittransfer-kv-group-member-add-success-adduser"
ParserVersion = v1.0.0
Conditions = [
"""MOVEitDMZ"""
"""Add User"""
]
},

{
Vendor = "Ipswitch"
Product = "MoveIt Transfer"
TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
"""\s:\s+({operation}[^,]+),\s+ID:"""
"""\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""TargetName:\s+(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)),"""
"""TargetID:\s+({dest_user_sid}[^,]+)"""
"""({operation}Change User Password)"""
]
Name = "ipswitch-moveittransfer-kv-user-password-modify-success-pwdfailed"
ParserVersion = v1.0.0
Conditions = [
"""MOVEitDMZ"""
"""Change User Password"""
]
},
${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-user-unlock-success-auditor
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""User account unlocked"""
    ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
"""msg=Account unlocked for user\s*({user_ou}[^$]+?).\s*description="""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
      Name = questsoftware-caad-cef-group-member-add-success-nestedmemberadd
      ParserVersion = "v1.0.0"
      Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""Nested member added to group"""
      ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was added to group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-group-member-add-success-memberadd
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""Member added to group"""
      ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was added to group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-user-lock-success-auditor
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""User account locked"""
    ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-group-member-add-success-usermemberadd
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""User member-of added"""
     ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was added to the group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-group-member-remove-success-nestedmemberremove
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""Nested member removed from group"""
     ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=\s*[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was removed from group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-group-member-remove-success-memberremove
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""Member removed from group"""
     ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=\s*[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was removed from group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-group-member-remove-success-usermemberremove
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""User member-of removed"""
     ]
     Fields = ${QuestParserTemplates.quest-change-auditor-events.Fields}[
       """msg=\s*[^\\]+[\\\/]*({account_id}[^(]+)[^=]+?was removed from the group\s[^\\]+[\\\/]*({group_name}\S+)\s"""
     ]
},

${QuestParserTemplates.quest-change-auditor-events}{
     Name = questsoftware-caad-cef-user-password-modify-success-pwdchanged
     ParserVersion = "v1.0.0"
     Conditions = [
"""CEF:"""
"""Quest Software"""
"""|Change Auditor|"""
"""|Active Directory|"""
"""User password changed"""
   ]
},

{
Vendor = Ipswitch
Product = MoveIt Transfer
TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Fields = [
  """({time}\w+\s+\d+ \d+:\d+:\d+)"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
  """\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
  """\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
  """\s:\s+({operation}[^,]+),\s+ID:"""
  """\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\sMessage:\s*({failure_reason}[^,\."]+)"""
]
Name = ipswitch-moveittransfer-kv-endpoint-authentication-fail-moveit
Conditions = [
  """AgentBrand: MOVEit"""
  """authentication failed"""
]
ParserVersion = "v1.0.0"
},
{
  Name = "ipswitch-moveittransfer-kv-endpoint-login-fail-signon"
  ParserVersion = "v1.0.0"
  Vendor = "Ipswitch"
  Product = "MoveIt Transfer"
  TimeFormat = ["MMM dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
"""AgentBrand: MOVEit"""
"""FAILED: Sign On"""
]
  Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
"""\s:\s+({operation}[^,]+),\s+ID:"""
"""\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sMessage:\s*({failure_reason}[^,\.\"]+)"""
  ]
},
{
  Name = "ipswitch-moveittransfer-kv-endpoint-login-fail-signon-1"
  ParserVersion = "v1.0.0"
  Vendor = "Ipswitch"
  Product = "MoveIt Transfer"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""MOVEitDMZ"""
"""FAILED: Sign On""" 
]
  Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""
"""\s\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""\sIPAddress:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""User\s'(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|Automation|({full_name}[^']+))?'\s\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)?\)"""
"""\s:\s+({operation}[^,]+),\s+ID:"""
"""\sUsername:\s*(Automation|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sMessage:\s*({failure_reason}.+?)\s*$"""
  ]
},
{
  Name = "apc-a-str-endpoint-login-success-webuser"
  ParserVersion = "v1.0.0"
  Vendor = "APC"
  Product = "APC"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" Web user """ 
""" logged in from """ 
]
  Fields = [
"""<\d+>(\w+\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))"""
"""Web user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)'"""
"""\slogged in from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\.?\s+"""
  ]
},

{
Name = "delinea-secretserver-cef-user-switch-success-checkout"
Vendor = "Delinea"
Product = "Secret Server"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""|Thycotic Software|"""
"""|SECRET - CHECKOUT|"""
"""Item Name:"""
]
Fields = [
"""\d{2}:\d{2}:\d{2} ({dest_host}({host}[\w\-.]+)) CEF:"""
"""\srt=({time}\d+)"""
"""\srt=({time}\w+ \d{2} \d{4} \d{2}:\d{2}:\d{2})"""
"""\sdvc=({dest_host}({host}[^\s]+))"""
"""\sdvchost=({dest_host}({host}[^\s]+))"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=(({domain}[^\\\s]+?)(\\+))?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sfname=((({account_domain}({dest_domain}[^\\=\s]+))(\\)+)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({=account_domain}({=dest_domain}[^=\\]+))(\\+))?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+="""
"""cs3=({safe_value}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "delinea-centrifyztps-kv-user-switch-success-granted"
Vendor = "Delinea"
Product = "Centrify Zero Trust Privilege Services"
TimeFormat = "epoch_sec"
Conditions = [
"""Centrify Suite|dzdo"""
"""dzdo granted"""
]
Fields = [
"""utc=({time}\d{10})"""
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w.\-]+)\s"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\d+\|\d+\|({event_name}.+?)\|\d"""
"""status=({result}.+?)\s\w+="""
"""pid=({process_id}\d+)"""
"""service=({service_name}.+?)\s\w+="""
"""runas=({account}({dest_user}.+?))\s\w+="""
"""EntityName=({object}.+?)\s*$"""
"""command=({process_path}({process_dir}.*?)(\/+({process_name}[^\/]+?))?)\s*(\w+=|$)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "securenvoy-semfa-kv-endpoint-login-fail-denied"
Vendor = "SecurEnvoy"
Product = "SecurEnvoy Multi-Factor Authentication"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""UserID="""
"""ClientIP="""
"""RemoteID="""
"""Access Denied"""
]
Fields = [
"""({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s""",
"""UserID=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+)|({=user}[^\s]+))\sAccess\s({auth_method}Denied)\s({failure_reason}.+?)\sClientIP=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\sRemoteID=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""TORVMVERIFY01\s({server_name}[^\s]+)"""
]
ParserVersion = "v1.0.0"
},

${mimecast-json-template.mimecast-json-event}{
Name = "mimecast-seg-cef-app-login-success-audittype"
Vendor = "Mimecast"
Product = "Mimecast Secure Email Gateway"
Conditions = [ """"auditType":"User Logged On"""", """"eventInfo":""", """"eventTime":""", """"category":""" ]
Fields = ${mimecast-json-template.mimecast-json-event.Fields}[
"""\"eventTime\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+)"""
"""\WdestinationServiceName=(|({event_subtype}[^=]+?))(\s+\w+=|\s*$)"""
"""\Wdproc=(|({dproc}[^=]+?))(\s+\w+=|\s*$)"""
"""\"auditType\":\"({operation}[^\"]+)"""
"""({result}success)"""
"""({app}Mimecast Email Security)"""
"""Application:\s*({service_name}[^,]+)"""
"""\WIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\"user\":\"({email_address}[^\"]+)"""
"""\"user(A|a)gent\"\s*:\s*\"({user_agent}[^\"]+?)\"\s*[,\}\]]"""
"""exa_regex=({result}(?i)success)"""
"""exa_regex=Remote IP is\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
"""exa_regex=Application:\s*({service_name}[^,]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "shibboleth-s-str-endpoint-login-success-saml"
Vendor = "Shibboleth"
Product = "Shibboleth"
TimeFormat = "yyyyMMdd'T'HHmmssZ"
Conditions = [
  """shibboleth:"""
  """:SAML:"""
]
Fields = [
  """({time}\d{8}T\d{6}Z)\|(|({action}({request_binding}[^\|]+)))\|[^\|]*\|(|({relying_party_id}[^\|]+))\|([^\|]*\|){4}(|({principal_name}[^\|]+))\|"""
  """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|\s*"""
  """\d{8}T\d{6}Z\|([^\|]*\|){7}(({email_address}(?!\d+)[^\@]+\@[^\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|"""
]
ParserVersion = "v1.0.0"
},

{
Name = "epic-siem-cef-endpoint-login-success-security"
Vendor = "Epic"
Product = "Epic SIEM"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CEF:"""
  """|Epic|Security-SIEM|"""
  """|AUTHENTICATION|"""
]
Fields = [
  """CEF:([^\|]*\|){5}({operation}[^\|]+)"""
  """({host}[\w\-.]+)\s+CEF:"""
  """LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """workstationID=({dest_host}[\w\-.]+)"""
  """shost=({src_host}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"
},

{
Name = "delinea-centrifyas-kv-endpoint-login-success-pam"
Vendor = "Delinea"
Product = "Centrify Authentication Service"
TimeFormat = "epoch_sec"
Conditions = [
  """Centrify Suite"""
  """|PAM|"""
  """granted|"""
]
Fields = [
  """utc=({time}\d{10})"""
  """\sahost=({host}[^=]+?)\s+\w+="""
  """\sclient=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(\(none\)|({src_host}[^=]+?)))(\||\s+\w+=)""",
  """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\d+\|\d+\|({event_name}.+?)\|\d"""
  """status=({result}.+?)\s\w+="""
  """pid=({process_id}\d+)"""
  """service=({service_name}[^=]+?)\s\w+="""
]
ParserVersion = "v1.0.0"
},

{
Name = "netwrix-auditor-xml-file-success-action"
Vendor = "Netwrix"
Product = "Netwrix Auditor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions =  [ """<EventRecordID>""", """ Action : """, """ ObjectType : """, """ What : """ ]
Fields = [
  """When\s*:\s*({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""
  """<Computer>({host}[\w\-.]+)"""
  """>({event_code}\d+)<\/EventID>"""
  """<EventRecordID>({event_id}.+?)<\/EventRecordID>"""
  """Action\s*:\s*({access}.+?)\s*Message\s*:"""
  """Where\s*:\s*({dest_host}[\w\-.]+)"""
  """ObjectType\s*:\s*({file_type}.+?)\s*Who\s*:"""
  """Who\s*:\s*(({domain}[^\\\s]+)\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """What\s*:\s*(|({file_path}({file_dir}[^\"]*?)[\\\/]*({file_name}[^\\\"]+?(\.({file_ext}[^\\\.\s\"]+))?)))\s*When\s*:"""
  """Workstation\s*:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Details\s*:"""
]
ParserVersion = "v1.0.0"
}

{
Name = "varonis-dsp-leef-file-success-datadvantage"
Vendor = "Varonis"
Product = "Varonis Data Security Platform"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a","MMM dd yyyy HH:mm:ss"]
Conditions = [
  """LEEF:"""
  """|Varonis|DatAdvantage|"""
]
Fields = [
  """devTime=({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
  """accountName=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """domain=(|({domain}.+?))\s+(\w+=|$)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)"""
  """Event_Type=({event_code}({access}.+?))\s+(\w+=|$)"""
  """Event_Status=({result}.+?)\s+(\w+=|$)"""
  """Affected_Object=(|({file_path}(({file_dir}[^=]+?)\\+)?({file_name}[^\\]+?(\.({file_ext}[^\.\s]+))?)))\s+(\w+=|$)"""
  """Affected_Object_Path=(|({file_path}.+?))\s+(\w+=|$)"""
  """Affected_Object_Path=({file_dir}.+?)\\[^\\]+?\s+(\w+=|$)"""
  """cat=({category}[^=]+?)\s+(\w+=|$)"""
  """DatAdvantage\|[^\\]+?\|({additional_info}({alert_name}[^\\]+?))\|"""
  """Device_Name=({src_host}[\w\-.]+?)\s+(\w+=|$)"""
  """accountName=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """usrName=(({domain}[^\\]+)\\)?(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+?))\s+(\w+=|$)"""
  """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
]
ParserVersion = "v1.0.0"
},

{
  Name = "lastpass-l-sk4-app-login-success-actionlogin"
  Vendor = "LastPass"
  Product = "LastPass"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """Action":"Log in"""
    """dproc=EventReporting"""
    """destinationServiceName=LastPass"""
  ]
  Fields = [
    """\"Time\":\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """\"IP_Address\":\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
    """destinationServiceName=({app}[^=]+?)\s\w+="""
    """\"+Action\"+:\"+({action}[^\"]+)\"+"""
    """\"Username\"+:\"+({email_address}[^@]+@[^\.\"]+\.[^\"]+)"""
    """\"+Data\"+:\"+({additional_info}[^\"\}]+)"""
  ]
  ParserVersion = "v1.0.0"
}
}
```