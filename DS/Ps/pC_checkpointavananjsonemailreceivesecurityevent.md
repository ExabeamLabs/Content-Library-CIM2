#### Parser Content
```Java
{
Name = checkpoint-avanan-json-email-receive-securityevent
  ParserVersion = v1.0.0
  Conditions = [ """type":"avanan_security_event"""", """"tag"""", """"subject"""", """"sender_address"""",  """"is_incoming":true""" ]
  DupFields = ["email_address->orig_user"]


}
```