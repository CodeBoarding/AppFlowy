```mermaid
graph LR
    Document_Operations_and_Events["Document Operations and Events"]
    Document_Parsing_and_Conversion["Document Parsing and Conversion"]
    Document_Operations_and_Events -- "parses document formats using" --> Document_Parsing_and_Conversion
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Coordinates rich text documents, block hierarchy parsing, document data transformations, and reminder tracking.

### Document Operations and Events
Handles document lifecycle operations, event dispatching, snapshot management, and collaborative document synchronization.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-document.src.manager.DocumentManager`:54-62
- `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser`:8-13
- `frontend.rust-lib.flowy-document.src.event_handler.convert_data_to_document_internal`:173-186



**Source Files:**

- `frontend/rust-lib/flowy-document/build.rs`
  - `frontend.rust-lib.flowy-document.build.main` (L1-L7) - Function
- `frontend/rust-lib/flowy-document/src/document.rs`
  - `frontend.rust-lib.flowy-document.src.document.subscribe_document_changed` (L11-L45) - Function
  - `frontend.rust-lib.flowy-document.src.document.subscribe_document_snapshot_state` (L47-L63) - Function
  - `frontend.rust-lib.flowy-document.src.document.subscribe_document_sync_state` (L65-L78) - Function
- `frontend/rust-lib/flowy-document/src/document_data.rs`
  - `frontend.rust-lib.flowy-document.src.document_data.DocumentDataPB.from` (L6-L32) - Function
  - `frontend.rust-lib.flowy-document.src.document_data.DocumentData.from` (L36-L61) - Function
  - `frontend.rust-lib.flowy-document.src.document_data.BlockPB.from` (L65-L75) - Function
  - `frontend.rust-lib.flowy-document.src.document_data.ChildrenPB.from` (L79-L81) - Function
- `frontend/rust-lib/flowy-document/src/entities.rs`
  - `frontend.rust-lib.flowy-document.src.entities.EncodedCollabPB` (L20-L25) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.OpenDocumentPayloadPB` (L28-L31) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.OpenDocumentParams` (L33-L35) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.OpenDocumentPayloadPB.try_into` (L39-L45) - Method
  - `frontend.rust-lib.flowy-document.src.entities.DocumentRedoUndoPayloadPB` (L49-L52) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentRedoUndoParams` (L54-L56) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentRedoUndoPayloadPB.try_into` (L60-L65) - Method
  - `frontend.rust-lib.flowy-document.src.entities.DocumentRedoUndoResponsePB` (L69-L78) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.UploadFileParamsPB` (L81-L93) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.UploadedFilePB` (L96-L104) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DownloadFilePB` (L107-L115) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DeleteFilePB` (L118-L122) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.CreateDocumentPayloadPB` (L125-L131) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.CreateDocumentParams` (L133-L136) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.CreateDocumentPayloadPB.try_into` (L140-L149) - Method
  - `frontend.rust-lib.flowy-document.src.entities.CloseDocumentPayloadPB` (L153-L156) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.CloseDocumentParams` (L158-L160) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.CloseDocumentPayloadPB.try_into` (L164-L169) - Method
  - `frontend.rust-lib.flowy-document.src.entities.ApplyActionPayloadPB` (L173-L179) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ApplyActionParams` (L181-L184) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ApplyActionPayloadPB.try_into` (L188-L198) - Method
  - `frontend.rust-lib.flowy-document.src.entities.DocumentDataPB` (L202-L211) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentTextPB` (L214-L217) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.BlockPB` (L219-L240) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.Block.from` (L243-L257) - Function
  - `frontend.rust-lib.flowy-document.src.entities.MetaPB` (L261-L266) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ChildrenPB` (L269-L272) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.BlockActionPB` (L275-L281) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.BlockActionPayloadPB` (L284-L305) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.BlockActionTypePB` (L308-L315) - Enum
  - `frontend.rust-lib.flowy-document.src.entities.BlockActionTypePB.default` (L318-L320) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DeltaTypePB` (L324-L328) - Enum
  - `frontend.rust-lib.flowy-document.src.entities.DeltaTypePB.default` (L330-L332) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DocEventPB` (L336-L345) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.BlockEventPB` (L348-L351) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.BlockEventPayloadPB` (L354-L366) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ExportType` (L369-L375) - Enum
  - `frontend.rust-lib.flowy-document.src.entities.ExportType.from` (L378-L389) - Function
  - `frontend.rust-lib.flowy-document.src.entities.EditPayloadPB` (L393-L400) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ExportDataPB` (L403-L409) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ConvertType` (L412-L415) - Enum
  - `frontend.rust-lib.flowy-document.src.entities.ConvertType.from` (L418-L426) - Function
  - `frontend.rust-lib.flowy-document.src.entities.ConvertDataPayloadPB` (L433-L439) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ConvertDataParams` (L441-L444) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.ConvertDataPayloadPB.try_into` (L448-L452) - Method
  - `frontend.rust-lib.flowy-document.src.entities.RepeatedDocumentSnapshotMetaPB` (L456-L459) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSnapshotMetaPB` (L462-L471) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSnapshotPB` (L474-L480) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSnapshotStatePB` (L483-L486) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSyncStatePB` (L489-L492) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSyncState` (L495-L501) - Enum
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSyncStatePB.from` (L504-L512) - Function
  - `frontend.rust-lib.flowy-document.src.entities.TextDeltaPayloadPB` (L516-L525) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.TextDeltaParams` (L527-L531) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.TextDeltaPayloadPB.try_into` (L535-L546) - Method
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSnapshotMeta` (L549-L553) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentSnapshotData` (L555-L558) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessStatesPB` (L561-L564) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessStatesPB.from` (L567-L573) - Function
  - `frontend.rust-lib.flowy-document.src.entities.UpdateDocumentAwarenessStatePB` (L577-L584) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessStatePB` (L587-L598) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessStatePB.from` (L601-L609) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessUserPB` (L613-L618) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessUserPB.from` (L621-L626) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessSelectionPB` (L630-L635) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessPositionPB` (L638-L643) - Struct
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessSelection.from` (L646-L651) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessSelectionPB.from` (L655-L660) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessPosition.from` (L664-L669) - Function
  - `frontend.rust-lib.flowy-document.src.entities.DocumentAwarenessPositionPB.from` (L673-L678) - Function
- `frontend/rust-lib/flowy-document/src/event_handler.rs`
  - `frontend.rust-lib.flowy-document.src.event_handler.upgrade_document` (L28-L35) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.get_encode_collab_handler` (L39-L51) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.create_document_handler` (L54-L65) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.open_document_handler` (L69-L81) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.close_document_handler` (L83-L92) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.get_document_data_handler` (L96-L105) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.get_document_text_handler` (L107-L116) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.apply_action_handler` (L119-L131) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.create_text_handler` (L134-L146) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.apply_text_delta_handler` (L149-L163) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.convert_data_to_document` (L165-L171) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.convert_data_to_document_internal` (L173-L186) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.redo_handler` (L188-L205) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.undo_handler` (L207-L224) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.can_undo_redo_handler` (L226-L242) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.get_snapshot_meta_handler` (L244-L253) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.get_snapshot_data_handler` (L255-L263) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.BlockAction.from` (L266-L271) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.BlockActionType.from` (L275-L284) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.BlockActionPayload.from` (L288-L296) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.BlockEventPB.from` (L300-L305) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.BlockEventPayloadPB.from` (L309-L316) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.DeltaTypePB.from` (L320-L326) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.DocEventPB.from` (L330-L339) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.convert_document_handler` (L381-L411) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.convert_data_to_json_handler` (L426-L438) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.upload_file_handler` (L442-L468) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.download_file_handler` (L471-L482) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.delete_file_handler` (L485-L492) - Function
  - `frontend.rust-lib.flowy-document.src.event_handler.set_awareness_local_state_handler` (L494-L505) - Function
- `frontend/rust-lib/flowy-document/src/event_map.rs`
  - `frontend.rust-lib.flowy-document.src.event_map.init` (L12-L55) - Function
  - `frontend.rust-lib.flowy-document.src.event_map.DocumentEvent` (L59-L140) - Enum
- `frontend/rust-lib/flowy-document/src/manager.rs`
  - `frontend.rust-lib.flowy-document.src.manager.DocumentUserService` (L39-L44) - Interface
  - `frontend.rust-lib.flowy-document.src.manager.DocumentUserService.user_id` (L40-L40) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentUserService.device_id` (L41-L41) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentUserService.workspace_id` (L42-L42) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentUserService.collab_db` (L43-L43) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentSnapshotService` (L46-L52) - Interface
  - `frontend.rust-lib.flowy-document.src.manager.DocumentSnapshotService.get_document_snapshot_metas` (L47-L50) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentSnapshotService.get_document_snapshot` (L51-L51) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager` (L54-L62) - Struct
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.drop` (L65-L67) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.new` (L71-L87) - Function
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.collab_builder` (L89-L94) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_encoded_collab_with_view_id` (L97-L112) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.initialize` (L114-L119) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.initialize_after_sign_up` (L127-L130) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.initialize_after_open_workspace` (L132-L135) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.initialize_after_sign_in` (L138-L141) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.handle_reminder_action` (L143-L149) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.persistence` (L151-L156) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.create_document` (L163-L193) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.collab_for_document` (L195-L219) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.editable_document` (L222-L232) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.create_document_instance` (L238-L298) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_document_data` (L300-L304) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_document_text` (L305-L310) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_document` (L314-L325) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.open_document` (L327-L339) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.close_document` (L341-L365) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.delete_document` (L367-L377) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.set_document_awareness_local_state` (L380-L402) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_document_snapshot_meta` (L405-L422) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_document_snapshot` (L424-L433) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.upload_file` (L436-L448) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.download_file` (L450-L454) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.delete_file` (L456-L460) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.is_doc_exist` (L462-L473) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.storage_service_upgrade` (L475-L480) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_cloud_service` (L484-L486) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.get_file_storage_service` (L489-L491) - Method
  - `frontend.rust-lib.flowy-document.src.manager.DocumentManager.restore_document_from_removing` (L493-L501) - Method
  - `frontend.rust-lib.flowy-document.src.manager.doc_state_from_document_data` (L504-L525) - Function
- `frontend/rust-lib/flowy-document/src/notification.rs`
  - `frontend.rust-lib.flowy-document.src.notification.DocumentNotification` (L7-L15) - Enum
  - `frontend.rust-lib.flowy-document.src.notification.i32.from` (L18-L20) - Function
  - `frontend.rust-lib.flowy-document.src.notification.DocumentNotification.from` (L23-L31) - Function
  - `frontend.rust-lib.flowy-document.src.notification.document_notification_builder` (L35-L40) - Function
- `frontend/rust-lib/flowy-document/src/parse.rs`
  - `frontend.rust-lib.flowy-document.src.parse.NotEmptyStr` (L2-L2) - Struct
  - `frontend.rust-lib.flowy-document.src.parse.NotEmptyStr.parse` (L5-L10) - Function
  - `frontend.rust-lib.flowy-document.src.parse.NotEmptyVec` (L14-L14) - Struct
  - `frontend.rust-lib.flowy-document.src.parse.NotEmptyVec.parse` (L17-L22) - Function
- `frontend/rust-lib/flowy-document/src/parser/document_data_parser.rs`
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser` (L8-L13) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.new` (L16-L21) - Function
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.to_html_with_json` (L24-L35) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.to_text_with_json` (L38-L44) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.to_html` (L47-L50) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.to_text` (L53-L56) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.to_json` (L59-L71) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.block_to_nested_block` (L73-L129) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.get_delta` (L131-L141) - Method
  - `frontend.rust-lib.flowy-document.src.parser.document_data_parser.DocumentDataParser.process_child_block` (L143-L156) - Method
- `frontend/rust-lib/flowy-document/src/parser/external/utils.rs`
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.JSONResult` (L66-L71) - Enum
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.flatten_element_to_block` (L74-L80) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.parse_plaintext_to_nested_block` (L83-L116) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.flatten_element_to_json` (L118-L166) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_default_element` (L168-L192) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_image_element` (L194-L204) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_code_element` (L206-L231) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_nested_element` (L234-L244) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_li_element` (L247-L274) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_node_summary_and_details` (L284-L311) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_heading_element` (L313-L343) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_inline_element` (L346-L359) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.process_node_children` (L361-L395) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.get_attributes_with_style` (L399-L438) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.get_delta_attributes_for` (L453-L499) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.node_to_delta` (L504-L519) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.get_tag_name` (L522-L524) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.get_node_attrs` (L526-L528) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.find_attribute_value` (L530-L536) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.find_attribute_value_from_attrs` (L538-L546) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.find_child_node` (L548-L558) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.utils.delta_to_json` (L560-L562) - Function
- `frontend/rust-lib/flowy-document/src/parser/json/block.rs`
  - `frontend.rust-lib.flowy-document.src.parser.json.block.SerdeBlock` (L13-L20) - Struct
- `frontend/rust-lib/flowy-document/src/parser/utils.rs`
  - `frontend.rust-lib.flowy-document.src.parser.utils.get_delta_for_block` (L10-L18) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.get_delta_for_selection` (L20-L28) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.slice_delta` (L30-L57) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.delta_to_text` (L58-L64) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.delta_to_html` (L66-L72) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.convert_nested_block_children_to_html` (L74-L100) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.convert_insert_delta_from_json` (L102-L104) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.required_not_empty_str` (L106-L111) - Function
  - `frontend.rust-lib.flowy-document.src.parser.utils.serialize_color_attribute` (L113-L126) - Function
- `frontend/rust-lib/flowy-document/src/reminder.rs`
  - `frontend.rust-lib.flowy-document.src.reminder.DocumentReminderAction` (L5-L9) - Enum
  - `frontend.rust-lib.flowy-document.src.reminder.DocumentReminder` (L12-L14) - Struct
  - `frontend.rust-lib.flowy-document.src.reminder.DocumentReminder.try_from` (L19-L23) - Function


### Document Parsing and Conversion
Parses external formats like HTML, plaintext, and JSON into structured document block models.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser`
- `frontend.rust-lib.flowy-document.src.parser.external.parser.ExternalDataToNestedJSONParser`:7-12
- `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock`:251-259



**Source Files:**

- `frontend/rust-lib/flowy-document/src/parser/external/parser.rs`
  - `frontend.rust-lib.flowy-document.src.parser.external.parser.ExternalDataToNestedJSONParser` (L7-L12) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.external.parser.ExternalDataToNestedJSONParser.new` (L15-L20) - Function
  - `frontend.rust-lib.flowy-document.src.parser.external.parser.ExternalDataToNestedJSONParser.to_nested_block` (L30-L39) - Method
- `frontend/rust-lib/flowy-document/src/parser/json/parser.rs`
  - `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser` (L12-L12) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser.json_str_to_document` (L17-L39) - Function
  - `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser.generate_blocks` (L41-L63) - Function
  - `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser.generate_text_map` (L65-L70) - Function
  - `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser.generate_children_map` (L72-L93) - Function
  - `frontend.rust-lib.flowy-document.src.parser.json.parser.JsonToDocumentParser.block_to_block_pb` (L95-L122) - Function
- `frontend/rust-lib/flowy-document/src/parser/parser_entities.rs`
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.SelectionPB` (L17-L26) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.RangePB` (L29-L35) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ParseTypePB` (L44-L53) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDocumentPayloadPB` (L61-L70) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDocumentResponsePB` (L73-L80) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.Selection` (L82-L86) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.Range` (L88-L91) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ParseType` (L93-L97) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDocumentParams` (L99-L103) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ParseType.any_enabled` (L106-L108) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.Selection.from` (L112-L118) - Function
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.Range.from` (L122-L127) - Function
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ParseType.from` (L131-L137) - Function
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDocumentPayloadPB.try_into` (L141-L152) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.InsertDelta` (L156-L161) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.InsertDelta.to_text` (L164-L166) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.InsertDelta.to_html` (L168-L247) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock` (L251-L259) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock.eq` (L264-L276) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock.new` (L280-L282) - Function
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock.add_child` (L284-L286) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock.convert_to_html` (L288-L450) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.NestedBlock.convert_to_text` (L452-L495) - Method
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertBlockToHtmlParams` (L498-L501) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.InputType` (L504-L508) - Enum
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDataToJsonPayloadPB` (L511-L518) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDataToJsonParams` (L520-L523) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDataToJsonResponsePB` (L526-L529) - Struct
  - `frontend.rust-lib.flowy-document.src.parser.parser_entities.ConvertDataToJsonPayloadPB.try_into` (L533-L538) - Method




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)