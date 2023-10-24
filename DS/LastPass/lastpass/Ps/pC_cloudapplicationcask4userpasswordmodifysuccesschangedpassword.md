#### Parser Content
```Java
{
Name = "cloudapplication-ca-sk4-user-password-modify-success-changedpassword"
Vendor = "LastPass"
Product = "LastPass"
TimeFormat = "epoch"
Conditions = [
""" suser="""
"""destinationServiceName ="""
""""Action":"Password Changed""""
]
Fields = [
"""\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)"""
"""\Wend=({time}\d{13})"""
"""\Wdproc=({process_name}.+?)(\s+\w+=|\s*$)"""
"""\Wfname=(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}.+?))(\s+\w+=|\s*$)"""
"""\Wmsg=({additional_info}.+?)(\s+\w+=|\s*$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wsuser=({email_address}[^@\s]+@[^@\s]+)"""
"""\Wsuser=({full_name}\w+(\s+\w+)+)"""
]
ParserVersion = "v1.0.0"


}
```