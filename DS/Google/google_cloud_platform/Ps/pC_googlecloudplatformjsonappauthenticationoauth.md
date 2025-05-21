#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-authentication-oauth
  Vendor = Google
  Product = Google Cloud Platform
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""jsonPayload":""",  """"type":"oauth-authorization"""",""""login_required"""","""dproc=Cloud PubSub"""]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """"hostname":"({host}[^"]+)"""
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"type":"({category}[^"]+)"""
    """"user_agent":"({user_agent}[^"]+)"""
    """destinationServiceName =({app}[^=]+?)\s\w+=""",
	  """"region":"({region}[^"]+)"""",
    """"(description|message)":\s*"?({additional_info}[^}"]+)""""
    """"project_id":"({project_id}[^"]+)"""",
    """"log_name":"({log_name}[^"]+)""""
    """"oauthError":"({failure_reason}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```