#### Parser Content
```Java
{
Name = openai-chatgpt-json-ai-conversation-delete-clp
  ParserVersion = v1.0.0
  Conditions = [ """"type":"CHATGPT_WORKSPACE"""", """"type":"AUDIT_LOG"""", """"action":"CONVERSATION_DELETE"""" ]

openai-json-audit-clp = {
    Vendor = OpenAI
    Product = ChatGPT
    ExtractionType = json
    TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
    Fields = [
      """exa_json_path=$.principal.id,exa_field_name=workspace_id"""
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_json_path=$.conversation.id,exa_field_name=conversation_id"""
      """exa_json_path=$.action_data.conversation_id,exa_field_name=conversation_id"""
      """exa_json_path=$.action_data.shared_conversation_id,exa_field_name=conversation_id"""
      """exa_json_path=$.conversation.gpt_id,exa_field_name=ai_agent_id"""
      """exa_json_path=$.conversation.title,exa_field_name=additional_info"""
      """exa_json_path=$.actor.user_email,exa_field_name=email_address"""
      """exa_json_path=$.actor.user_id,exa_field_name=user_id"""
      """exa_json_path=$.actor.type,exa_field_name=user_type"""
      """exa_json_path=$.action_privilege,exa_field_name=user_privilege_category"""
      """exa_json_path=$.type,exa_field_name=event_name"""
      """exa_json_path=$.action,exa_field_name=operation"""
      """exa_json_path=$.action_result,exa_field_name=result"""
      """exa_json_path=$.message.author.type,exa_field_name=message_author_type"""
      """exa_json_path=$.message.content.value,exa_field_name=llm_request"""
      """exa_json_path=$.message.author.tools_used,exa_field_name=ai_tool_name"""
      """exa_json_path=$.message.files[*].name,exa_field_name=file_name"""
      """exa_json_path=$.message.files[*].id,exa_field_name=file_id"""
      """exa_json_path=$..action_name,exa_field_name=ai_function_name"""
      """exa_json_path=$.message.content.annotations[*].action_name,exa_field_name=ai_function_name""" 
      """exa_json_path=$.action_data.deleted_user_id,exa_field_name=dest_user_id"""
      """exa_json_path=$.action_data.user_id,exa_field_name=dest_user_id"""
      """exa_json_path=$.action_data.email_address,exa_field_name=dest_email_address"""
      """exa_json_path=$.request_metadata.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.request_metadata.client_user_agent,exa_field_name=user_agent"""
      """exa_json_path=$.action_data.role,exa_field_name=role_name"""
      """exa_json_path=$.action_data.group_id,exa_field_name=group_id"""
      """exa_json_path=$.action_data.name,exa_field_name=group_name"""
      """exa_json_path=$.action_data.new_name,exa_field_name=group_name"""
      """exa_json_path=$.action_data.email_addresses,exa_field_name=email_recipients"""
      """exa_json_path=$.action_data.email_addresses,exa_field_name=recipients"""
      """exa_json_path=$.action_data.email_addresses[0],exa_field_name=dest_email_address"""
      """exa_json_path=$.action_data.added_user_id,exa_field_name=member"""
      """exa_json_path=$.action_data.removed_user_id,exa_field_name=member"""
      """exa_json_path=$.action_data.added_user_id,exa_field_name=dest_user_id"""

    openai-json-audit-clp = {
    Vendor = OpenAI
    Product = ChatGPT
    ExtractionType = json
    TimeFormat = ["epoch_sec", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
    Fields = [
      """exa_json_path=$.principal.id,exa_field_name=workspace_id"""
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_json_path=$.conversation.id,exa_field_name=conversation_id"""
      """exa_json_path=$.action_data.conversation_id,exa_field_name=conversation_id"""
      """exa_json_path=$.action_data.shared_conversation_id,exa_field_name=conversation_id"""
      """exa_json_path=$.conversation.gpt_id,exa_field_name=ai_agent_id"""
      """exa_json_path=$.conversation.title,exa_field_name=additional_info"""
      """exa_json_path=$.actor.user_email,exa_field_name=email_address"""
      """exa_json_path=$.actor.user_id,exa_field_name=user_id"""
      """exa_json_path=$.actor.type,exa_field_name=user_type"""
      """exa_json_path=$.action_privilege,exa_field_name=user_privilege_category"""
      """exa_json_path=$.type,exa_field_name=event_name"""
      """exa_json_path=$.action,exa_field_name=operation"""
      """exa_json_path=$.action_result,exa_field_name=result"""
      """exa_json_path=$.message.author.type,exa_field_name=message_author_type"""
      """exa_json_path=$.message.content.value,exa_field_name=llm_request"""
      """exa_json_path=$.message.author.tools_used,exa_field_name=ai_tool_name"""
      """exa_json_path=$.message.files[*].name,exa_field_name=file_name"""
      """exa_json_path=$.message.files[*].id,exa_field_name=file_id"""
      """exa_json_path=$..action_name,exa_field_name=ai_function_name"""
      """exa_json_path=$.message.content.annotations[*].action_name,exa_field_name=ai_function_name""" 
      """exa_json_path=$.action_data.deleted_user_id,exa_field_name=dest_user_id"""
      """exa_json_path=$.action_data.user_id,exa_field_name=dest_user_id"""
      """exa_json_path=$.action_data.email_address,exa_field_name=dest_email_address"""
      """exa_json_path=$.request_metadata.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$.request_metadata.client_user_agent,exa_field_name=user_agent"""
      """exa_json_path=$.action_data.role,exa_field_name=role_name"""
      """exa_json_path=$.action_data.group_id,exa_field_name=group_id"""
      """exa_json_path=$.action_data.name,exa_field_name=group_name"""
      """exa_json_path=$.action_data.new_name,exa_field_name=group_name"""
      """exa_json_path=$.action_data.email_addresses,exa_field_name=email_recipients"""
      """exa_json_path=$.action_data.email_addresses,exa_field_name=recipients"""
      """exa_json_path=$.action_data.email_addresses[0],exa_field_name=dest_email_address"""
      """exa_json_path=$.action_data.added_user_id,exa_field_name=member"""
      """exa_json_path=$.action_data.removed_user_id,exa_field_name=member"""
      """exa_json_path=$.action_data.added_user_id,exa_field_name=dest_user_id"""

    ]
  }
}
```