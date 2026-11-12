```mermaid
graph LR
    Upload_Management_and_Caching["Upload Management and Caching"]
    Storage_Contracts_and_Chunking["Storage Contracts and Chunking"]
    Upload_Management_and_Caching -- "implements contracts and uses byte chunking" --> Storage_Contracts_and_Chunking
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Manages binary asset uploads, chunked streaming, local file caching, and cloud blob storage syncing.

### Upload Management and Caching
Coordinates file upload tasks, SQLite upload state tracking, temporary disk caching, and progress event dispatching.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-storage.src.manager.StorageManager`:43-50
- `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl`:260-268
- `frontend.rust-lib.flowy-storage.src.uploader.FileUploader`:58-65
- `frontend.rust-lib.flowy-storage.src.uploader.UploadTaskQueue`:21-24
- `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage`:8-10



**Source Files:**

- `frontend/rust-lib/flowy-storage/build.rs`
  - `frontend.rust-lib.flowy-storage.build.main` (L1-L7) - Function
- `frontend/rust-lib/flowy-storage/src/entities.rs`
  - `frontend.rust-lib.flowy-storage.src.entities.RegisterStreamPB` (L4-L7) - Struct
  - `frontend.rust-lib.flowy-storage.src.entities.QueryFilePB` (L10-L13) - Struct
  - `frontend.rust-lib.flowy-storage.src.entities.FileStatePB` (L16-L22) - Struct
- `frontend/rust-lib/flowy-storage/src/event_handler.rs`
  - `frontend.rust-lib.flowy-storage.src.event_handler.upgrade_storage_manager` (L7-L14) - Function
  - `frontend.rust-lib.flowy-storage.src.event_handler.register_stream_handler` (L17-L25) - Function
  - `frontend.rust-lib.flowy-storage.src.event_handler.query_file_handler` (L28-L38) - Function
- `frontend/rust-lib/flowy-storage/src/event_map.rs`
  - `frontend.rust-lib.flowy-storage.src.event_map.init` (L8-L14) - Function
  - `frontend.rust-lib.flowy-storage.src.event_map.FileStorageEvent` (L18-L25) - Enum
- `frontend/rust-lib/flowy-storage/src/file_cache.rs`
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage` (L8-L10) - Struct
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.new` (L14-L22) - Function
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.generate_temp_file_path_with_name` (L25-L27) - Method
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.create_temp_file_from_existing` (L31-L52) - Method
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.create_temp_file_from_bytes` (L56-L65) - Method
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.write_to_temp_file` (L69-L73) - Method
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.read_from_temp_file` (L77-L82) - Method
  - `frontend.rust-lib.flowy-storage.src.file_cache.FileTempStorage.delete_temp_file` (L85-L88) - Method
- `frontend/rust-lib/flowy-storage/src/manager.rs`
  - `frontend.rust-lib.flowy-storage.src.manager.StorageUserService` (L35-L40) - Interface
  - `frontend.rust-lib.flowy-storage.src.manager.StorageUserService.user_id` (L36-L36) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageUserService.workspace_id` (L37-L37) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageUserService.sqlite_connection` (L38-L38) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageUserService.get_application_root_dir` (L39-L39) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager` (L43-L50) - Struct
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.drop` (L53-L55) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.new` (L59-L136) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.register_file_progress_stream` (L138-L151) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.query_file_state` (L153-L174) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.initialize` (L176-L182) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.initialize_after_open_workspace` (L184-L190) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.update_network_reachable` (L192-L198) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.disable_storage_write_access` (L200-L203) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.enable_storage_write_access` (L205-L208) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.subscribe_file_state` (L210-L219) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.get_file_state` (L223-L228) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageManager.get_all_tasks` (L230-L233) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.prepare_upload_task` (L236-L258) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl` (L260-L268) - Struct
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl.delete_object` (L272-L319) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl.download_object` (L321-L347) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl.create_upload` (L349-L433) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl.start_upload` (L435-L457) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl.resume_upload` (L459-L479) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.StorageServiceImpl.subscribe_file_progress` (L481-L506) - Method
  - `frontend.rust-lib.flowy-storage.src.manager.create_upload_record` (L509-L539) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.start_upload` (L542-L743) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.handle_upload_error` (L745-L766) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.resume_upload` (L769-L784) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.upload_part` (L788-L821) - Function
  - `frontend.rust-lib.flowy-storage.src.manager.complete_upload` (L823-L891) - Function
- `frontend/rust-lib/flowy-storage/src/notification.rs`
  - `frontend.rust-lib.flowy-storage.src.notification.StorageNotification` (L7-L12) - Enum
  - `frontend.rust-lib.flowy-storage.src.notification.i32.from` (L15-L17) - Function
  - `frontend.rust-lib.flowy-storage.src.notification.make_notification` (L21-L23) - Function
- `frontend/rust-lib/flowy-storage/src/sqlite_sql.rs`
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.UploadFileTable` (L14-L25) - Struct
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.UploadFilePartTable` (L30-L34) - Struct
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.is_upload_file_exist` (L36-L52) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.insert_upload_file` (L54-L70) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.update_upload_file_upload_id` (L72-L90) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.update_upload_file_completed` (L92-L99) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.is_upload_exist` (L101-L107) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.is_upload_completed` (L109-L126) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.delete_upload_file` (L129-L135) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.delete_upload_file_by_file_id` (L137-L167) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql._delete_upload_file` (L169-L184) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.delete_all_upload_parts` (L186-L192) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.insert_upload_part` (L194-L202) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.select_latest_upload_part` (L204-L214) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.select_upload_parts` (L216-L224) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.batch_select_upload_file` (L226-L240) - Function
  - `frontend.rust-lib.flowy-storage.src.sqlite_sql.select_upload_file` (L242-L258) - Function
- `frontend/rust-lib/flowy-storage/src/uploader.rs`
  - `frontend.rust-lib.flowy-storage.src.uploader.Signal` (L15-L19) - Enum
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTaskQueue` (L21-L24) - Struct
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTaskQueue.new` (L27-L32) - Function
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTaskQueue.queue_task` (L33-L37) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTaskQueue.remove_task` (L39-L55) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader` (L58-L65) - Struct
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.drop` (L68-L70) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.new` (L74-L87) - Function
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.all_tasks` (L89-L92) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.queue_tasks` (L94-L100) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.pause` (L102-L106) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.disable_storage_write` (L108-L113) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.enable_storage_write` (L115-L120) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.resume` (L122-L128) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploader.process_next` (L131-L249) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploaderRunner` (L252-L252) - Struct
  - `frontend.rust-lib.flowy-storage.src.uploader.FileUploaderRunner.run` (L255-L294) - Function
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTask` (L298-L311) - Enum
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTask.retry_count` (L314-L319) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTask.fmt` (L323-L328) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTask.eq` (L334-L353) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTask.partial_cmp` (L357-L359) - Method
  - `frontend.rust-lib.flowy-storage.src.uploader.UploadTask.cmp` (L363-L379) - Method


### Storage Contracts and Chunking
Defines cloud and local storage service traits, file upload progress entities, and multipart byte chunking utilities.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService`:11-37
- `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService`:9-86
- `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes`:14-19
- `frontend.rust-lib.flowy-storage-pub.src.storage.ProgressNotifier`:100-104
- `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageObject`:100-104



**Source Files:**

- `frontend/rust-lib/flowy-storage-pub/src/chunked_byte.rs`
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes` (L14-L19) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes.from_file` (L23-L43) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes.next_chunk` (L46-L70) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes.set_offset` (L73-L83) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes.total_chunks` (L86-L88) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes.current_offset` (L91-L93) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.ChunkedBytes.fmt` (L97-L106) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.split_into_chunks` (L110-L112) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.calculate_offsets` (L114-L125) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_chunked_bytes_small_file` (L134-L157) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_chunked_bytes_large_file` (L160-L188) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_set_offset` (L191-L214) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_partial_chunk` (L217-L246) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_invalid_offset` (L249-L268) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_exact_multiple_chunk_file` (L271-L297) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_small_file_less_than_chunk_size` (L300-L326) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_file_slightly_larger_than_chunk_size` (L329-L358) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_large_file_with_many_chunks` (L361-L387) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.chunked_byte.tests.test_file_with_exact_chunk_size` (L390-L416) - Function
- `frontend/rust-lib/flowy-storage-pub/src/cloud.rs`
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService` (L9-L86) - Interface
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.get_object_url` (L18-L18) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.put_object` (L28-L28) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.delete_object` (L38-L38) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.get_object` (L48-L48) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.get_object_url_v1` (L49-L54) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.parse_object_url_v1` (L57-L57) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.create_upload` (L59-L66) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.upload_part` (L68-L76) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageCloudService.complete_upload` (L78-L85) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.ObjectIdentity` (L88-L92) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.ObjectValue` (L95-L98) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageObject` (L100-L104) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.ObjectValueSupabase` (L106-L109) - Enum
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.ObjectValueSupabase.mime_type` (L112-L119) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageObject.from_file` (L130-L138) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageObject.from_bytes` (L148-L160) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.cloud.StorageObject.file_size` (L167-L172) - Method
- `frontend/rust-lib/flowy-storage-pub/src/storage.rs`
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService` (L11-L37) - Interface
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService.delete_object` (L12-L12) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService.download_object` (L14-L14) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService.create_upload` (L16-L21) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService.start_upload` (L23-L23) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService.resume_upload` (L25-L30) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.StorageService.subscribe_file_progress` (L32-L36) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgressReceiver` (L39-L42) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgressReceiver.deref` (L47-L49) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgressReceiver.deref_mut` (L53-L55) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileUploadState` (L59-L63) - Enum
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgress` (L66-L71) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgress.new_progress` (L74-L81) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgress.new_error` (L83-L90) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.storage.FileProgress.fmt` (L94-L96) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.ProgressNotifier` (L100-L104) - Struct
  - `frontend.rust-lib.flowy-storage-pub.src.storage.ProgressNotifier.new` (L107-L114) - Function
  - `frontend.rust-lib.flowy-storage-pub.src.storage.ProgressNotifier.subscribe` (L116-L121) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.ProgressNotifier.notify` (L123-L126) - Method
  - `frontend.rust-lib.flowy-storage-pub.src.storage.CreatedUpload` (L130-L133) - Struct




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)