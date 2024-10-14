#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-fullycompliant
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """Host Checker Compliance Result""", """['Fully Compliant']""", """PulseSecure:""" ]
    Fields = [
      """({result}Fully Compliant)""",
      """ for user \['(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'\]""",
      """ on host \['({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'\]"""
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+PulseSecure:"""
    ]
    DupFields = [ "user->account" ]
  

}
```