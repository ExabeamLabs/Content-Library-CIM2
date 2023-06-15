#### Parser Content
```Java
{
Name = oracle-db-xml-database-login-success-dbauth
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """<DB_User>"""
  """<OS_User>"""
  """<Userhost>"""
  """<OS_Process>"""
  """Authenticated by:"""
]
Fields = [
  """<Extended_Timestamp>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+\w)</Extended_Timestamp>"""
  """<DB_User>(\/|({db_user}.+?))</DB_User>"""
  """<OS_User>({user}.+?)</OS_User>"""
  """<Userhost>({src_host}[^\<]+)</Userhost>"""
  """<OS_Process>({process_id}\d+)</OS_Process>"""
  """<Session_Id>({session_id}\d+)</Session_Id>"""
  """<Returncode>({result}.+?)</Returncode>"""
  """<DBID>({db_name}.+?)</DBID>"""
  """PROTOCOL=({protocol}[^\)]+)"""
  """HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """PORT=({src_port}\d+)"""
]
DupFields = [
  "user->user"
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```