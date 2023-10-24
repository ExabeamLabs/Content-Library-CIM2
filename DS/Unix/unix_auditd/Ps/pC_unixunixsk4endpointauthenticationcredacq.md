#### Parser Content
```Java
{
Name = unix-unix-sk4-endpoint-authentication-credacq
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":"CRED_ACQ"""", """PAM:setcred""", """"logger.account":""", """"message":""" ]

unix-template-dl = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\Wrt=({time}\d{13})""",
      """\Wdvc=({host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """CEF:([^\|]*\|){4}({additional_info}[^\|]+)""",
      """CEF:([^\|]*\|){5}({event_code}[^\|]+)""",
      """\WeventId=({alert_id}\d+)""",
      """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
    
}
```