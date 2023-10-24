#### Parser Content
```Java
{
Name = armorblox-ab-json-email-threat
  Conditions = [ """"incident_type":"THREAT_INCIDENT_TYPE"""", """"resolution_state":""", """"remediation_actions":""" ]
  ParserVersion = "v1.0.0"

armorblox-email = {
  Vendor = Armorblox
  Product = Armorblox
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"date":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"title":"({email_subject}[^"]+)"""",
    """"original_sender_address":"({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"users":.+?"email":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """"app_name":"({app}[^"]+)"""",
    """"remediation_actions":\[?"({operation}[^"]+)"\]?""",
    """"folder_categories":\[?"({category}[^"]+)"\]?""",
    """"priority":"({priority}[^"]+)"""",
    """"incident_type":"({event_name}[^"]+)"""",
    """"attachment_list":\[?"({email_attachments}[^"]+)""""
   
}
```