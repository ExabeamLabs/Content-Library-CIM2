#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-4769-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
"""A Kerberos service ticket was requested"""
""""event_id":"4769""""
""""additional_information-TicketOptions":""""
]
Fields = [
"""({event_name}A Kerberos service ticket was requested)"""
""""time":"({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))""""
""""host":"({host}[^"]+)\s*"""
"""({event_code}4769)"""
""""account_information-AccountName":"\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*"""
""""account_information-AccountDomain":"\s*({domain}[^"]+)\s*"""
""""service_information-ServiceName":"\s*({dest_host}\S+\$)\s*""""
""""service_information-ServiceName":"\s*({service_name}[^"]+)\s*""""
""""network_information-ClientAddress":"\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""additional_information-FailureCode":"\s*({result_code}[^"]+)\s*""""
""""additional_information-TicketOptions":"\s*({ticket_options}[^"]+)""""
""""additional_information-TicketEncryptionType":"\s*({ticket_encryption_type}[^"]+)\s*""""
]
ParserVersion = "v1.0.0"


}
```