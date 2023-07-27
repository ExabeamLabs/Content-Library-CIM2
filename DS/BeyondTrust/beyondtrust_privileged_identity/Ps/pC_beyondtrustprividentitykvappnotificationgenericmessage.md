#### Parser Content
```Java
{
Name = beyondtrust-prividentity-kv-app-notification-genericmessage
  Conditions = [ """sEventType=""", """sEventID="EVENT_ID_WEBAPP_GENERIC_MESSAGE"""", """sOriginatingApplicationName ="Privileged Identity"""" ]
  ParserVersion = "v1.0.0"

lieberman-events = {
      Vendor = BeyondTrust
      Product = BeyondTrust Privileged Identity
      TimeFormat = "yyyy-dd-MM'T'HH:mm:ss"
      Fields = [
        """({host}\S+)\s+<Event"""
        """dwAppSpecificEventID="({event_code}\d+)"""
        """sEventID="({event_name}[^"]+)"""
        """sOriginatingApplicationName ="({app}[^"]+)"""
        """sOriginatingSystem="({src_host}[^"]+)"""
        """sOriginatingAccount="(({account_domain}[^\\]+)[\\]+)?({account}[^\s"]+)""""
        """dtPostTime="({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
        """sMessage="({additional_info}[^"]+)"""
        """sLoginName ="(({domain}[^\\]+)[\\]+)?({user}[\w\.\-]{1,40}\$?)""""
# job_id is removed
        """sIpAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        
}
```