#### Parser Content
```Java
{
Name = microsoft-o365-json-email-emailsend
Vendor = Microsoft
Product = Office 365
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
  """"SenderAddress"+:\s*"+(<>|\\+|({email_address}[^">,]+))"""
  """"MessageId"+:\s*"+({message_id}[^",]+)""""
  """"ToIP"+:\s*"+?(?:null|({dest_ip}[a-fA-F\d.:]+))"""
  """"FromIP"+:\s*"+?(?:null|({src_ip}[a-fA-F\d.:]+))"""
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