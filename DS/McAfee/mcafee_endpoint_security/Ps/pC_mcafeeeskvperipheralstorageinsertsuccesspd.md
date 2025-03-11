#### Parser Content
```Java
{
Name = mcafee-es-kv-peripheral-storage-insert-success-pd
  Conditions = [ """DeviceClassName ="Portable Devices""", """InsertionTime="""", """destination="""", """RulesToDisplay="""" ]
  ParserVersion = "v1.0.0"

splunk-mcafee-usb-insert-activity = {
      Vendor = McAfee
      Product = McAfee Endpoint Security
      TimeFormat = "yyyy-MM-dd HH:mm:ss"
      Fields = [
        """InsertionTime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
        """RulesToDisplay="({operation}[^"]+)""",
        """IP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """\sName ="({dest_host}[^"]+)""",
        """Username_NTLM="((({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
        """USBVendorId="(\s*|({device_id}[^"]+))"""",
        """DeviceName ="({device_class}[^"]+)""",
        """\sFileName ="({file_name}[^"]+)""",
        """({action}Block)""",
        """TotalContentSize="({bytes}\d+)"""
        """DeviceClassName ="({device_class}[^"=]+)"""

      ]
      DupFields = ["operation->operation_details"]
    }

    mcafee-http-session-2 = {
    Vendor = McAfee
    Product = McAfee Web Gateway
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd HH:mm:ss"]
    Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s({host}[\w\-.]+)\s(\S+\s+){4}"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}[^"]+)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^?";]+)","({uri_path}\/[^;\?]*?)?)","({action}OBSERVED|PROXIED|DENIED)",("[^"]*",){3}"({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",){4}"({http_response_code}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))""""
    """"({user}[\w\.\-\!\#\^\~]{1,40}\$?)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({method}GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE|CERTVERIFY)",""""
   """"(GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE|CERTVERIFY)","({bytes_in}\d+)","({bytes_out}\d+)","(({url}[^\?";]+)","({uri_path}\/[^\?]*?)?)","({action}OBSERVED|PROXIED|DENIED)","""
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)","({protocol}[^"]+)","({categories}({category}[^,"]+?)(,[^"]*)?)",("[^"]*",)""""
   """",("[^"]*",){6}"({http_response_code}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",("[^"]*",){2}"({browser}[^"]+)","[^"]*","(\s*|({user_agent}[^"]+))""""
    ]
    DupFields = ["url->web_domain"]
    }

cef-skyhigh_security-secure_web_gateway = {
  Vendor = Skyhigh Security
  Product = Secure Web Gateway
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss.SSS"
  Fields = [
    """\d\d:\d\d:\d\d\s({host}[\w\-.]+)\smwg:""",
    """Timestamp=({time}\d{1,2}\/\w{3}\/\d{4}:\d\d:\d\d:\d\d\.\d{3})\s""",
    """\sUser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """\sAction=({action}[^\s]+)\s"""
  
}
```