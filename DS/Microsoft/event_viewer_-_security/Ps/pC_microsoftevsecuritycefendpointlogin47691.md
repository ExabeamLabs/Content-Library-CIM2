#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-4769-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""CEF:"""
""""eventID":"4769""""
"""A Kerberos service ticket was requested"""
]
Fields = [
""""systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
""""computer":"({host}[\w\-.]+)"""
""""message":"({event_name}[^"]+?)\s*""""
""""eventID":"({event_code}\d+)"""
""""eventRecordID":"({event_id}\d+)"""
""""severityValue":"({result}[^"]+?)\s*""""
""""targetSid":"({user_sid}[^"\s]+?)\s*""""
""""targetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*""""
""""targetUserName":"({email_address}[^"\s@]+@[^"\s@]+?)\s*""""
""""targetDomainName":"({domain}[^"\s]+?)\s*""""
""""serviceName":"({service_name}[^"\s]+?)\s*""""
""""serviceName":"({dest_host}[\w\-.]+?\$)\s*""""
""""ticketEncryptionType":"({ticket_encryption_type}[^"\s]+?)\s*""""
""""ticketOptions":"({ticket_options}[^"\s]+?)\s*""""
""""status":"({result_code}[^"]+?)\s*""""
""""ipAddress":"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""ipPort":"({src_port}\d+)"""
]
DupFields = [ "email_address->dest_email_address", "user_sid->dest_user_sid", "user->dest_user", "domain->dest_domain" ]
ParserVersion = "v1.0.0"


}
```