#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-fail-partiallycompliant
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """Host Checker Compliance Result""", """['Partially Compliant']""", """PulseSecure:""" ]
    Fields = [
      """({result}Partially Compliant)""",
      """failed_reasons: \['({failure_reason}.+?)'\]""",
      """ for user \['(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-]+))'\]""",
      """ on host \['({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'\]"""
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+PulseSecure:"""
      """msg="({event_code}\w+)"""
    ]
 

}
```