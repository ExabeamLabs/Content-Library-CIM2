#### Parser Content
```Java
{
Name = okta-amfa-json-app-activity-published
Conditions = [
  """core.user_auth.session_created_using_token"""
  """"published":"""
]
ParserVersion = "v1.0.0"

q-okta-app-login.Fields}[
    """Client ID:\s*({src_host}[^"\s]+)""",
  ]
  ParserVersion = "v1.0.0"
},

${OktaParserTemplates.q-okta-app-login}{
  Name = okta-amfa-json-app-login-success-activedirectory
  Conditions = [ """"message"":""Active Directory authentication succeeded""", """"published"":""""" ]
  ParserVersion = "v1.0.0"
},

${OktaParserTemplates.q-okta-app-login}{
  Name = okta-amfa-json-app-login-success-signin
  Conditions = [ """"message"":""Sign-in successful""", """"published"":""""" ]
  ParserVersion = "v1.0.0"
},

${OktaParserTemplates.q-okta-app-login}{
  Name = okta-amfa-json-app-login-success-iwaauthentication
  Conditions = [ """"message"":""IWA authentication result: SUCCESS""", """"published"":""""" ]
  Fields = ${OktaParserTemplates.q-okta-app-login.Fields}[
    """({event_name}IWA authentication)""",
  ]
  ParserVersion = "v1.0.0"
},

${OktaParserTemplates.q-okta-app-login}{
  Name = okta-amfa-json-app-login-fail-signin
  Conditions = [ """"message"":""Sign-in Failed""", """"published"":""""" ]
  Fields = ${OktaParserTemplates.q-okta-app-login.Fields}[
    """Sign-in Failed\s*-\s*({failure_reason}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"
},

${OktaParserTemplates.q-okta-app-login}{
  Name = okta-amfa-mix-app-login-fail-activedirectory
  Conditions = [ """message""", """Active Directory authentication failed""", """published"":""""" ]
  Fields = ${OktaParserTemplates.q-okta-app-login.Fields}[
    """"Active Directory authentication failed:\s*({failure_reason}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = okta-amfa-kv-app-login-success-singlesignon
  Vendor = Okta
  Product = Okta Adaptive MFA
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """|OKTA|OKTA Identity Provider|""","""|Application Access|""","""msg=User performed single sign on to app"""]
  Fields = [
	"""start=({time}\d\d\d\d\-\d+\-\d+T\d+:\d+:\d+:\d+)""",
	"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	"""instance=({host}[^,]+)""",
    """duid=({user}[\w\.\-]{1,40}\$?)""",
    """duid=[^@,]+@({domain}[^,.]+)""",
    """destinationServiceName =({app}[^,]+)""",
    """cs3=({user_agent}.+?), \w+=""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = workday-wd-json-app-login-success-startnewsession-1
  Vendor = Workday
  Product = Workday
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """:"workday"""", """"wd_systemaccount":""", """"wd_ipaddress":""",""""wd_activitycategory":""", """Start New Session""", """"wd_task":"""]
  Fields = [
    """timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """hostname":"({host}[^"]+?)"""",
    """device_product":"({app}[^"]+?)"""",
    """wd_systemaccount":"({domain}[^\/]+?)\s\/\s({full_name}[^"]+?)"""",
    """wd_task":"({operation}[^"]+?)"""",
    """wd_target":"({object}[^"]+?)"""",
    """wd_useragent":"({user_agent}[^"]+?)"""",
    """wd_ipaddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
   ]
   DupFields = [ "full_name->user" ]
   ParserVersion = v1.0.0
}

{
Vendor = "Okta"
Product = "Okta Adaptive MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
"""\d+:\d+ ({host}[^\s]+) \{"""
""""published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""action":\s*\{.*?"objectType":\s*"({operation}[^"]+)".+?\}"""
""""action":\s*\{.*?"objectType":\s*"[^"]*?({result}error)".+?\}"""
""""categories":\s*\["({operation}[^"]+)""""
""""actors":\[.*?\{.*?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"[^\{\}]+?"objectType":"User".*?\}"""
""""actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"displayName":\s*"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))""""
""""displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+?))\s*"[^\}\]]*"objectType":"User""""
""""actors":\[.*?\{.*?"login":"({user}[\w\.\-]{1,40}\$?)"[^\{\}]+?"objectType":"User".*?\}"""
""""actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({user}[\w\.\-]{1,40}\$?)""""
""""actors":\[.*?\{.*?"login":"({email_address}[^"\s@]+@[^"\s@]+)"[^\{\}]+?"objectType":"User".*?\}"""
""""actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({email_address}[^"\s@]+@[^"\s@]+)""""
""""actors":\[.*?\{.*?"login":"[^@]+@({email_domain}[^"]+)"[^\{\}]+?"objectType":"User".*?\}"""
""""actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"[^@]+@({email_domain}[^"]+)""""
""""targets":\[.*?\{.*?"login":"({dest_user}[^"]+)"[^\{\}]+?"objectType":"User".*?\}"""
""""targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({dest_user}[^"]+)""""
""""targets":\[.*?\{.*?"login":"({account_name}[^@\s"]+)@({dest_domain}[^"]+)"[^\{\}]+?"objectType":"User".*?\}"""
""""targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*({account_name}[^@\s"]+)@({dest_domain}[^"]+)""""
""""actors":\[.*?\{.*?"id":"({user_agent}[^"]+)"[^\{\}]+?"objectType":"Client".*?\}"""
""""actors":\s*\[\{[^\]]*?"objectType":\s*"Client"[^\]]*?"id":\s*"({user_agent}[^"]+)""""
""""message":\s*"({additional_info}[^"]+?)\s*""""
"""({app}Okta)"""
"""destinationServiceName({app}.+?)\s*\w+="""
""""targets":\[.*?\{.*?"displayName":"({app}[^"]+)"[^\{\}]+?"objectType":"AppInstance".*?\}"""
""""targets":\s*\[\{[^\]]*?"objectType":\s*"AppInstance"[^\]]*?"displayName":\s*"({app}[^"]+)""""
""""type":"AppInstance"[^\}\]]*"displayName":"({app}[^"]+?)\s*""""
"""requestUri":\s*"({request_uri}[^"]+?)\s*""""
""""id":"({object}[^"]+)"[^\}\]]*"objectType":"AppInstance""""
""""objectType":"AppInstance"[^\}\]]*"id":"({object}[^"]+)""""
]
DupFields = [
"dest_user->account_name"
"dest_domain->account_domain"
]
Name = "okta-amfa-json-user-enable-success-published"
Conditions = [
""""User Activation""""
""""published":"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Okta"
Product = "Okta Adaptive MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
  """\d+:\d+ ({host}[^\s]+) \{"""
  """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"action":\s*\{.*?"objectType":\s*"({operation}[^"]+)".+?\}"""
  """"action":\s*\{.*?"objectType":\s*"[^"]*?({result}error)".+?\}"""
  """"categories":\s*\["({operation}[^"]+)""""
  """"actors":\[.*?\{.*?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"[^\{\}]+?"objectType":"User".*?\}"""
  """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"displayName":\s*"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))""""
  """"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+?))\s*"[^\}\]]*"objectType":"User""""
  """"actors":\[.*?\{.*?"login":"({user}[\w\.\-]{1,40}\$?)"[^\{\}]+?"objectType":"User".*?\}"""
  """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({user}[\w\.\-]{1,40}\$?)""""
  """"actors":\[.*?\{.*?"login":"({email_address}[^"\s@]+@[^"\s@]+)"[^\{\}]+?"objectType":"User".*?\}"""
  """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({email_address}[^"\s@]+@[^"\s@]+)""""
  """"actors":\[.*?\{.*?"login":"[^@]+@({email_domain}[^"]+)"[^\{\}]+?"objectType":"User".*?\}"""
  """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"[^@]+@({email_domain}[^"]+)""""
  """"targets":\[.*?\{.*?"login":"({dest_user}[^"]+)"[^\{\}]+?"objectType":"User".*?\}"""
  """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"({dest_user}[^"]+)""""
  """"targets":\[.*?\{.*?"login":"({account_name}[^@\s"]+)@({dest_domain}[^"]+)"[^\{\}]+?"objectType":"User".*?\}"""
  """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*({account_name}[^@\s"]+)@({dest_domain}[^"]+)""""
  """"actors":\[.*?\{.*?"id":"({user_agent}[^"]+)"[^\{\}]+?"objectType":"Client".*?\}"""
  """"actors":\s*\[\{[^\]]*?"objectType":\s*"Client"[^\]]*?"id":\s*"({user_agent}[^"]+)""""
  """"message":\s*"({additional_info}[^"]+?)\s*""""
  """({app}Okta)"""
  """destinationServiceName({app}.+?)\s*\w+="""
  """"targets":\[.*?\{.*?"displayName":"({app}[^"]+)"[^\{\}]+?"objectType":"AppInstance".*?\}"""
  """"targets":\s*\[\{[^\]]*?"objectType":\s*"AppInstance"[^\]]*?"displayName":\s*"({app}[^"]+)""""
  """"type":"AppInstance"[^\}\]]*"displayName":"({app}[^"]+?)\s*""""
  """requestUri":\s*"({request_uri}[^"]+?)\s*""""
  """"id":"({object}[^"]+)"[^\}\]]*"objectType":"AppInstance""""
  """"objectType":"AppInstance"[^\}\]]*"id":"({object}[^"]+)""""
]
DupFields = [
  "dest_user->account_name"
  "dest_domain->account_domain"
]
Name = okta-amfa-json-user-create-success-usercreation
Conditions = [
  """"User Creation""""
  """"published":"""
]
ParserVersion = "v1.0.0"
},

{
Name = "workday-wd-json-app-activity-success-appactivity"
Vendor = "Workday"
Product = "Workday"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """:"workday""""
  """"wd_systemaccount":"""
  """"wd_ipaddress":"""
  """"wd_activitycategory":"""
  """"wd_task":"""
]
Fields = [
  """timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """hostname":"({host}[^"]+?)""""
  """device_product":"({app}[^"]+?)""""
  """wd_systemaccount":"({domain}[^\/]+?)\s\/\s({full_name}[^"]+?)(\son behalf of\s[^"]+)?""""
  """wd_task":"({operation}[^"]+?)""""
  """wd_target":"({object}[^"]+?)""""
  """wd_useragent":"({user_agent}[^"]+?)""""
  """wd_ipaddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
]
ParserVersion = "v1.0.0"
},

{
Vendor = "Okta"
Product = "Okta Adaptive MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
  """\d+:\d+ ({host}[^\s]+) \{"""
  """"published":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """"ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"action":\s*\{.*?"objectType":\s*"({operation}[^"]+)".+?\}"""
  """"action":\s*\{.*?"objectType":\s*"[^"]*?({result}error)".+?\}"""
  """"categories":\s*\["({operation}[^"]+)""""
  """"actors":\[.*?\{.*?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"[^\{\}]+?"objectType":"User".*?\}"""
  """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"displayName":\s*"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))""""
  """"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+?))\s*"[^\}\]]*"objectType":"User""""
  """"actors":\[.*?\{.*?"login":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"[^\{\}]+?"objectType":"User".*?\}""",
  """"actors":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"""",
  """"targets":\[.*?\{.*?"login":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"[^\{\}]+?"objectType":"User".*?\}"""
  """"targets":\s*\[\{[^\{\}]*?"objectType":\s*"User"[^\]]*?"login":\s*"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))""""
  """"actors":\[.*?\{.*?"id":"({user_agent}[^"]+)"[^\{\}]+?"objectType":"Client".*?\}"""
  """"actors":\s*\[\{[^\]]*?"objectType":\s*"Client"[^\]]*?"id":\s*"({user_agent}[^"]+)""""
  """"message":\s*"({additional_info}[^"]+?)\s*""""
  """({app}Okta)"""
  """destinationServiceName({app}.+?)\s*\w+="""
  """"targets":\[.*?\{.*?"displayName":"({app}[^"]+)"[^\{\}]+?"objectType":"AppInstance".*?\}"""
  """"targets":\s*\[\{[^\]]*?"objectType":\s*"AppInstance"[^\]]*?"displayName":\s*"({app}[^"]+)""""
  """"type":"AppInstance"[^\}\]]*"displayName":"({app}[^"]+?)\s*""""
  """requestUri":\s*"({request_uri}[^"]+?)\s*""""
  """"id":"({object}[^"]+)"[^\}\]]*"objectType":"AppInstance""""
  """"objectType":"AppInstance"[^\}\]]*"id":"({object}[^"]+)""""
]
DupFields = [
  "dest_user->account_name"
]
Name = okta-amfa-json-app-activity-published
Conditions = [
  """core.user_auth.session_created_using_token"""
  """"published":"""
]
ParserVersion = "v1.0.0"
}
${OktaParserTemplates.s-okta-app-login}{
  Name = okta-amfa-json-app-login-success-signon
  ParserVersion = v1.0.0
  Conditions = [ """"eventType":"policy.evaluate_sign_on"""" ]
  Fields = ${OktaParserTemplates.s-okta-app-login.Fields} [
    """"displayMessage":"({additional_info}[^"]+)"""
    """"eventType":"({operation}[^"]+)"""
  
}
```