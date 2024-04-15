#### Parser Content
```Java
{
Name = "f5-apm-cef-vpn-login-success-newsessionfromclient"
Vendor = "F5"
Product = "F5 Access Policy Manager"
TimeFormat = "epoch"
Conditions = [
"""|F5|APM|"""
"""|New session from client|"""
"""01490500:5:"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\smsg=[^=]*? from client IP ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? [^=]*? at VIP ({src_translated_ip}[a-fA-F\d.:]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\scs4=({session_id}.+?)(?:\s+[\w.]+=|\s*$)"""
"""\sdvc=({host}[a-fA-F\d.:]+)"""
"""\sdvchost=({host}.+?)(?:\s+[\w.]+=|\s*$)"""
"""\sad\.VIPAddress=({src_translated_ip}[a-fA-F\d.:]+)"""
]
ParserVersion = "v1.0.0"


}
```