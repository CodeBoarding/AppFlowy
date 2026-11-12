```mermaid
graph LR
    Cloud_Backend_Service_Adapter["Cloud Backend Service Adapter"]
    Local_Offline_Services_Provider["Local Offline Services Provider"]
    Server_Abstraction_Interfaces["Server Abstraction Interfaces"]
    Cloud_Backend_Service_Adapter -- "implements server abstraction" --> Server_Abstraction_Interfaces
    Local_Offline_Services_Provider -- "references user session trait" --> Cloud_Backend_Service_Adapter
    Local_Offline_Services_Provider -- "implements server abstraction" --> Server_Abstraction_Interfaces
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Provides server abstraction implementations for local offline mode and AppFlowy Cloud backend services.

### Cloud Backend Service Adapter
Implements cloud-based synchronization and services connecting AppFlowy to remote servers over HTTP and WebSocket protocols.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer`:49-60
- `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser`:18-31



**Source Files:**

- `frontend/rust-lib/flowy-server/src/af_cloud/define.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser` (L18-L31) - Interface
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.workspace_id` (L20-L20) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.workspace_type` (L21-L21) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.user_id` (L23-L23) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.is_local_mode` (L24-L24) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.get_sqlite_db` (L26-L26) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.get_collab_db` (L28-L28) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.LoggedUser.application_root_dir` (L30-L30) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl` (L34-L34) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.logged_user` (L37-L42) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.user_id` (L47-L49) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.is_local_model` (L51-L53) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.workspace_id` (L55-L57) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.workspace_type` (L59-L61) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.sqlite_connection` (L63-L65) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.define.AIUserServiceImpl.application_root_dir` (L67-L69) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/chat.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl` (L23-L25) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.create_chat` (L32-L54) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.create_question` (L56-L77) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.create_answer` (L79-L98) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.stream_answer` (L100-L127) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_answer` (L129-L141) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_chat_messages` (L143-L157) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_question_from_answer_id` (L159-L177) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_related_message` (L179-L193) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.stream_complete` (L195-L210) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.embed_file` (L212-L223) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_chat_settings` (L225-L236) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.update_chat_settings` (L238-L250) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_available_models` (L252-L259) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.get_workspace_default_model` (L261-L268) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.chat.CloudChatServiceImpl.set_workspace_default_model` (L270-L282) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/database.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl` (L24-L27) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl.get_database_encode_collab` (L36-L65) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl.create_database_encode_collab` (L69-L87) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl.batch_get_database_encode_collab` (L90-L129) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl.get_database_collab_object_snapshots` (L131-L137) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl.summary_database_row` (L145-L162) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.database.AFCloudDatabaseCloudServiceImpl.translate_database_row` (L164-L183) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/document.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.document.AFCloudDocumentCloudServiceImpl` (L20-L23) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.document.AFCloudDocumentCloudServiceImpl.get_document_doc_state` (L31-L57) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.document.AFCloudDocumentCloudServiceImpl.get_document_snapshots` (L59-L66) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.document.AFCloudDocumentCloudServiceImpl.get_document_data` (L69-L100) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.document.AFCloudDocumentCloudServiceImpl.create_document_collab` (L102-L118) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/file_storage.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl` (L9-L14) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.new` (L17-L22) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.get_object_url` (L30-L37) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.put_object` (L39-L43) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.delete_object` (L45-L48) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.get_object` (L50-L56) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.get_object_url_v1` (L58-L69) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.parse_object_url_v1` (L71-L74) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.create_upload` (L76-L109) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.upload_part` (L111-L134) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.file_storage.AFCloudFileStorageServiceImpl.complete_upload` (L136-L157) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/folder.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl` (L28-L31) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_folder_snapshots` (L38-L44) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_folder_doc_state` (L47-L68) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.full_sync_collab_object` (L70-L86) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.batch_create_folder_collab_objects` (L88-L108) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.service_name` (L110-L112) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.publish_view` (L114-L146) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.unpublish_views` (L148-L158) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_publish_info` (L160-L167) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.set_publish_name` (L169-L189) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.set_publish_namespace` (L191-L201) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.list_published_views` (L203-L214) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_default_published_view_info` (L216-L227) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.set_default_published_view` (L229-L241) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.remove_default_published_view` (L243-L251) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_publish_namespace` (L253-L260) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.import_zip` (L262-L273) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.share_page_with_user` (L275-L286) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.revoke_shared_page_access` (L288-L300) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_shared_page_details` (L302-L313) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.folder.AFCloudFolderCloudServiceImpl.get_shared_views` (L315-L325) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/search.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.search.AFCloudSearchCloudServiceImpl` (L15-L18) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.search.AFCloudSearchCloudServiceImpl.document_search` (L27-L46) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.search.AFCloudSearchCloudServiceImpl.generate_search_summary` (L48-L60) - Method
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/user/cloud_service_impl.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl` (L44-L48) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.new` (L51-L61) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.sign_up` (L69-L74) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.sign_in` (L77-L83) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.sign_out` (L85-L89) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.delete_account` (L91-L95) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.generate_sign_in_url_with_email` (L97-L105) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.create_user` (L107-L118) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.sign_in_with_password` (L120-L131) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.sign_in_with_magic_link` (L133-L146) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.sign_in_with_passcode` (L148-L159) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.generate_oauth_url_with_provider` (L161-L169) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.update_user` (L171-L178) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_user_profile` (L181-L206) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.open_workspace` (L208-L213) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_all_workspace` (L215-L224) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.create_workspace` (L226-L236) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.patch_workspace` (L238-L255) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.delete_workspace` (L257-L262) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.invite_workspace_member` (L264-L283) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.list_workspace_invitations` (L285-L299) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.accept_workspace_invitations` (L301-L307) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.remove_workspace_member` (L309-L319) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.update_workspace_member` (L321-L333) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_members` (L335-L347) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_user_awareness_doc_state` (L350-L365) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.subscribe_user_update` (L367-L370) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.create_collab_object` (L372-L391) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.batch_create_collab_object` (L393-L418) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.leave_workspace` (L420-L425) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.subscribe_workspace` (L427-L446) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_member` (L448-L462) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_subscriptions` (L464-L471) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_subscription_one` (L473-L483) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.cancel_workspace_subscription` (L485-L502) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_plan` (L504-L514) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_usage` (L516-L526) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_billing_portal_url` (L528-L533) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.update_workspace_subscription_payment_period` (L535-L551) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_subscription_plan_details` (L553-L558) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.get_workspace_setting` (L560-L569) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.AFCloudUserAuthServiceImpl.update_workspace_setting` (L571-L584) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.get_admin_client` (L587-L613) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.user_sign_up_request` (L615-L620) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.user_sign_in_with_url` (L622-L648) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.to_user_workspace` (L650-L661) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.to_user_workspaces` (L663-L669) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.to_workspace_invitation` (L671-L681) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.cloud_service_impl.oauth_params_from_box_any` (L683-L692) - Function
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/user/dto.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.af_update_from_update_params` (L10-L23) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.user_profile_from_af_profile` (L25-L50) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.to_af_role` (L52-L58) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.from_af_role` (L60-L66) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.from_af_workspace_member` (L68-L76) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.to_workspace_invitation_status` (L78-L86) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.dto.from_af_workspace_invitation_status` (L88-L96) - Function
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/user/util.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.user.util.encryption_type_from_profile` (L5-L10) - Function
- `frontend/rust-lib/flowy-server/src/af_cloud/impls/util.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.impls.util.check_request_workspace_id_is_match` (L10-L31) - Function
- `frontend/rust-lib/flowy-server/src/af_cloud/server.rs`
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer` (L49-L60) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.new` (L63-L111) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.get_server_impl` (L113-L120) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.set_token` (L125-L130) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.set_ai_model` (L132-L135) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.subscribe_token_state` (L137-L164) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.set_enable_sync` (L166-L169) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.set_network_reachable` (L171-L173) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.user_service` (L175-L197) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.folder_service` (L199-L204) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.database_service` (L206-L211) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.database_ai_service` (L213-L218) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.document_service` (L220-L225) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.chat_service` (L227-L234) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.subscribe_ws_state` (L236-L238) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.get_ws_state` (L240-L242) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.collab_ws_channel` (L245-L260) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.file_storage` (L262-L267) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.search_service` (L269-L275) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AppFlowyCloudServer.set_tanvity_state` (L277-L279) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.spawn_ws_conn` (L286-L346) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.attempt_reconnect` (L354-L380) - Function
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AFServer` (L382-L385) - Interface
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AFServer.get_client` (L383-L383) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AFServer.try_get_client` (L384-L384) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AFServerImpl` (L388-L390) - Struct
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AFServerImpl.get_client` (L393-L395) - Method
  - `frontend.rust-lib.flowy-server.src.af_cloud.server.AFServerImpl.try_get_client` (L397-L408) - Method


### Local Offline Services Provider
Provides standalone local server implementations for workspace management, document editing, and search operations when offline.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer`:22-28



**Source Files:**

- `frontend/rust-lib/flowy-server/src/local_server/impls/chat.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl` (L33-L36) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_message_content` (L39-L46) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.upsert_message` (L48-L54) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.create_chat` (L59-L73) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.create_question` (L75-L91) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.create_answer` (L93-L108) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.stream_answer` (L110-L127) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_answer` (L129-L142) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_chat_messages` (L144-L167) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_question_from_answer_id` (L169-L182) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_related_message` (L184-L214) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.stream_complete` (L216-L227) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.embed_file` (L229-L246) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_chat_settings` (L248-L266) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.update_chat_settings` (L268-L286) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_available_models` (L288-L290) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.get_workspace_default_model` (L292-L294) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.LocalChatServiceImpl.set_workspace_default_model` (L296-L303) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.chat_message_from_row` (L306-L337) - Function
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.MessageIDGenerator` (L339-L341) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.MessageIDGenerator.new` (L344-L348) - Function
  - `frontend.rust-lib.flowy-server.src.local_server.impls.chat.MessageIDGenerator.next_id` (L350-L364) - Method
- `frontend/rust-lib/flowy-server/src/local_server/impls/database.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.impls.database.LocalServerDatabaseCloudServiceImpl` (L13-L15) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.database.LocalServerDatabaseCloudServiceImpl.get_database_encode_collab` (L19-L37) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.database.LocalServerDatabaseCloudServiceImpl.create_database_encode_collab` (L39-L47) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.database.LocalServerDatabaseCloudServiceImpl.batch_get_database_encode_collab` (L49-L56) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.database.LocalServerDatabaseCloudServiceImpl.get_database_collab_object_snapshots` (L58-L64) - Method
- `frontend/rust-lib/flowy-server/src/local_server/impls/document.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.impls.document.LocalServerDocumentCloudServiceImpl` (L8-L8) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.document.LocalServerDocumentCloudServiceImpl.get_document_doc_state` (L12-L23) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.document.LocalServerDocumentCloudServiceImpl.get_document_snapshots` (L25-L32) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.document.LocalServerDocumentCloudServiceImpl.get_document_data` (L34-L40) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.document.LocalServerDocumentCloudServiceImpl.create_document_collab` (L42-L49) - Method
- `frontend/rust-lib/flowy-server/src/local_server/impls/folder.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl` (L26-L30) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_folder_snapshots` (L34-L40) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_folder_doc_state` (L42-L70) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.full_sync_collab_object` (L72-L89) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.batch_create_folder_collab_objects` (L91-L97) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.service_name` (L99-L101) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.publish_view` (L103-L109) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.unpublish_views` (L111-L117) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_publish_info` (L119-L121) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.set_publish_name` (L123-L130) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.set_publish_namespace` (L132-L138) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.list_published_views` (L140-L145) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_default_published_view_info` (L147-L152) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.set_default_published_view` (L154-L160) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.remove_default_published_view` (L162-L164) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_publish_namespace` (L166-L168) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.import_zip` (L170-L172) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.share_page_with_user` (L174-L180) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.revoke_shared_page_access` (L182-L189) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_shared_page_details` (L191-L197) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.folder.LocalServerFolderCloudServiceImpl.get_shared_views` (L199-L204) - Method
- `frontend/rust-lib/flowy-server/src/local_server/impls/search.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.impls.search.LocalSearchServiceImpl` (L15-L20) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.search.LocalSearchServiceImpl.document_search` (L24-L51) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.search.LocalSearchServiceImpl.generate_search_summary` (L53-L82) - Method
- `frontend/rust-lib/flowy-server/src/local_server/impls/user.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl` (L41-L43) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.sign_up` (L47-L71) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.sign_in` (L73-L92) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.sign_out` (L94-L96) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.generate_sign_in_url_with_email` (L98-L103) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.create_user` (L105-L107) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.sign_in_with_password` (L109-L115) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.sign_in_with_magic_link` (L117-L123) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.sign_in_with_passcode` (L125-L131) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.generate_oauth_url_with_provider` (L133-L135) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.update_user` (L137-L143) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_user_profile` (L145-L153) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.open_workspace` (L155-L161) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_all_workspace` (L163-L167) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.create_workspace` (L169-L186) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.patch_workspace` (L188-L195) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.delete_workspace` (L197-L199) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_workspace_members` (L201-L208) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_user_awareness_doc_state` (L210-L225) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.create_collab_object` (L227-L233) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.batch_create_collab_object` (L235-L241) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_workspace_member` (L243-L278) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_workspace_usage` (L280-L299) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.get_workspace_setting` (L301-L333) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.LocalServerUserServiceImpl.update_workspace_setting` (L335-L356) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.impls.user.insert_collabs` (L359-L378) - Function
- `frontend/rust-lib/flowy-server/src/local_server/server.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer` (L22-L28) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.new` (L31-L43) - Function
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.stop` (L45-L50) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.set_token` (L55-L57) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.set_tanvity_state` (L59-L61) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.user_service` (L63-L67) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.folder_service` (L69-L74) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.database_service` (L76-L80) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.database_ai_service` (L82-L84) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.document_service` (L86-L88) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.chat_service` (L90-L95) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.search_service` (L97-L104) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.server.LocalServer.file_storage` (L106-L108) - Method
- `frontend/rust-lib/flowy-server/src/local_server/template/create_workspace.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.template.create_workspace.create_workspace_for_user` (L7-L35) - Function
  - `frontend.rust-lib.flowy-server.src.local_server.template.create_workspace.CreateWorkspaceCollab` (L37-L40) - Struct
- `frontend/rust-lib/flowy-server/src/local_server/uid.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.uid.IDGenerator` (L10-L14) - Struct
  - `frontend.rust-lib.flowy-server.src.local_server.uid.IDGenerator.new` (L17-L23) - Function
  - `frontend.rust-lib.flowy-server.src.local_server.uid.IDGenerator.next_id` (L25-L44) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.uid.IDGenerator.wait_next_millis` (L46-L51) - Method
  - `frontend.rust-lib.flowy-server.src.local_server.uid.IDGenerator.timestamp` (L53-L58) - Method
- `frontend/rust-lib/flowy-server/src/local_server/util.rs`
  - `frontend.rust-lib.flowy-server.src.local_server.util.default_encode_collab_for_collab_type` (L11-L47) - Function
- `frontend/rust-lib/flowy-server/src/util.rs`
  - `frontend.rust-lib.flowy-server.src.util.deserialize_null_or_default` (L13-L20) - Function
  - `frontend.rust-lib.flowy-server.src.util.tanvity_local_search` (L22-L49) - Function
  - `frontend.rust-lib.flowy-server.src.util.tanvity_document_to_search_document` (L51-L66) - Function


### Server Abstraction Interfaces
Defines the core server trait contracts, embedding interfaces, encryption helpers, and standard HTTP response types.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-server.src.server.AppFlowyServer`:62-152
- `frontend.rust-lib.flowy-server.src.server.EmbeddingWriter`:28-38
- `frontend.rust-lib.flowy-server.src.response.HttpResponse`:9-13



**Source Files:**

- `frontend/rust-lib/flowy-server/src/response.rs`
  - `frontend.rust-lib.flowy-server.src.response.HttpResponse` (L9-L13) - Struct
  - `frontend.rust-lib.flowy-server.src.response.HttpError` (L16-L19) - Struct
  - `frontend.rust-lib.flowy-server.src.response.HttpError.is_unauthorized` (L23-L25) - Method
  - `frontend.rust-lib.flowy-server.src.response.HttpError.fmt` (L29-L31) - Method
- `frontend/rust-lib/flowy-server/src/server.rs`
  - `frontend.rust-lib.flowy-server.src.server.EmbeddingWriter` (L28-L38) - Interface
  - `frontend.rust-lib.flowy-server.src.server.EmbeddingWriter.index_encoded_collab` (L29-L35) - Method
  - `frontend.rust-lib.flowy-server.src.server.EmbeddingWriter.index_unindexed_collab` (L37-L37) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyEncryption` (L40-L43) - Interface
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyEncryption.get_secret` (L41-L41) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyEncryption.set_secret` (L42-L42) - Method
  - `frontend.rust-lib.flowy-server.src.server.Arc.get_secret` (L49-L51) - Method
  - `frontend.rust-lib.flowy-server.src.server.Arc.set_secret` (L53-L55) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer` (L62-L152) - Interface
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.set_token` (L63-L63) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.set_tanvity_state` (L64-L64) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.set_ai_model` (L65-L67) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.subscribe_token_state` (L69-L71) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.set_enable_sync` (L77-L77) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.set_network_reachable` (L83-L83) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.user_service` (L93-L93) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.folder_service` (L101-L101) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.database_service` (L110-L110) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.database_ai_service` (L112-L112) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.document_service` (L120-L120) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.chat_service` (L122-L122) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.search_service` (L126-L126) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.subscribe_ws_state` (L128-L130) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.get_ws_state` (L132-L134) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.collab_ws_channel` (L137-L149) - Method
  - `frontend.rust-lib.flowy-server.src.server.AppFlowyServer.file_storage` (L151-L151) - Method
  - `frontend.rust-lib.flowy-server.src.server.EncryptionImpl` (L154-L156) - Struct
  - `frontend.rust-lib.flowy-server.src.server.EncryptionImpl.new` (L159-L163) - Function
  - `frontend.rust-lib.flowy-server.src.server.EncryptionImpl.get_secret` (L167-L169) - Method
  - `frontend.rust-lib.flowy-server.src.server.EncryptionImpl.set_secret` (L171-L173) - Method




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)