#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-failedpassword"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["MMM dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [
    """sshd["""
    """]: Failed password for """
  ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+)\s+(::ffff:)?({host}[\w\-.]+)\s+"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s+({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s"""
    """Message forwarded from ({host}[^\s:]+)"""
    """({event_code}ssh)"""
    """Failed password for (({email_address}[^@\s]+@[^\.\s]+\.[^\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) from (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """ port ({src_port}\d+)"""
    """({failure_reason}Failed password)"""
    """\s(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+))\ssshd\["""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```