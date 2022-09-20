#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-password-modify-4723-2
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """__li_source_path=""", """An attempt was made to change""","""eventid="4723"""" ]
  Fields = [
    """({event_name}An attempt was made to change an account's password)""",
    """__li_source_path="({host}[^"]+)"""",
    """({event_code}4723)""",
    """Subject.+?Security ID:\s+({user_sid}.+?)\s+Account Name""",
    """Subject.+?Account Name:\s+({user}.+?)\s+Account Domain""",
    """Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)""",
    """Target Account.+?Account Name:\s+({dest_user}.+?)\s+Account Domain:\s+({dest_domain}.+?)\s+Additional""",
    """keywords="({result}[^"]+)""""]
  DupFields = [ "host->dest_ip" ]
  ParserVersion = "v1.0.0"


}
```