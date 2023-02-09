#### Parser Content
```Java
{
Name = microsoft-o365-json-email-send-receive-emailsend
Vendor = Microsoft
Product = Microsoft 365
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"RecipientAddress""""
  """"SenderAddress""""
  """"MessageTraceId""""
  """"Subject": """
]
Fields = [
  """"Received"+:\s*"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d+)"""
  """"DateReceived":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)"""
  """"RecipientAddress"+:\s*"+({email_recipients}[^",]+)""""
  """"RecipientAddress"+:\s*"+({dest_email_address}[^"\s,;]+)"""
  """"SenderAddress"+:\s*"+(<>|\\+|({sender}[^">,]+))"""
  """"MessageId"+:\s*"+({message_id}[^",]+)""""
  """"ToIP"+:\s*"+?(?:null|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """"FromIP"+:\s*"+?(?:null|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """"Subject"+:\s*(?:"+|"+({email_subject}.+?)\s*)"+,\s*""""
  """"Size"+:\s*"?({bytes}\d+)"""
  """"Status"+:\s*"+({result}[^",]+)""""
  """"Organization"+:"+({host}[^",]+)"""
  """"MessageTraceId"+:\s*"+({alert_id}[^",]+)"""
  """src-account-name":"({account_name}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```