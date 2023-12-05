#### Parser Content
```Java
{
Name = checkpoint-avanan-json-email-send-securityevent
  ParserVersion = v1.0.0
  Conditions = [ """"eventtype":"avanan_security_event"""", """"tag"""", """"subject"""", """"sender_address"""", """"is_incoming":false""" ]
  DupFields = ["email_address->orig_user"]


}
```