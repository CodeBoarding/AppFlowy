```mermaid
graph LR
    Search_Query_Coordinator["Search Query Coordinator"]
    Index_Storage_and_Abstraction["Index Storage and Abstraction"]
    Search_Query_Coordinator -- "queries local index and cloud service" --> Index_Storage_and_Abstraction
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Powers local full-text search and remote search indexing using Tantivy schemas and query filters.

### Search Query Coordinator
Orchestrates multi-source search requests and streams local and cloud search results to clients.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-search.src.services.manager.SearchManager`:42-46
- `frontend.rust-lib.flowy-search.src.services.manager.SearchHandler`:26-36
- `frontend.rust-lib.flowy-search.src.document.local_search_handler.DocumentLocalSearchHandler`:19-21
- `frontend.rust-lib.flowy-search.src.document.cloud_search_handler.DocumentCloudSearchHandler`:21-24



**Source Files:**

- `frontend/rust-lib/flowy-search/build.rs`
  - `frontend.rust-lib.flowy-search.build.main` (L1-L7) - Function
- `frontend/rust-lib/flowy-search/src/document/cloud_search_handler.rs`
  - `frontend.rust-lib.flowy-search.src.document.cloud_search_handler.DocumentCloudSearchHandler` (L21-L24) - Struct
  - `frontend.rust-lib.flowy-search.src.document.cloud_search_handler.DocumentCloudSearchHandler.new` (L27-L35) - Function
  - `frontend.rust-lib.flowy-search.src.document.cloud_search_handler.DocumentCloudSearchHandler.search_type` (L40-L42) - Method
  - `frontend.rust-lib.flowy-search.src.document.cloud_search_handler.DocumentCloudSearchHandler.perform_search` (L44-L169) - Method
  - `frontend.rust-lib.flowy-search.src.document.cloud_search_handler.extract_icon` (L172-L183) - Function
- `frontend/rust-lib/flowy-search/src/document/local_search_handler.rs`
  - `frontend.rust-lib.flowy-search.src.document.local_search_handler.DocumentLocalSearchHandler` (L19-L21) - Struct
  - `frontend.rust-lib.flowy-search.src.document.local_search_handler.DocumentLocalSearchHandler.new` (L24-L26) - Function
  - `frontend.rust-lib.flowy-search.src.document.local_search_handler.DocumentLocalSearchHandler.search_type` (L31-L33) - Method
  - `frontend.rust-lib.flowy-search.src.document.local_search_handler.DocumentLocalSearchHandler.perform_search` (L35-L79) - Method
  - `frontend.rust-lib.flowy-search.src.document.local_search_handler.tanvity_item_to_local_search_item` (L82-L92) - Function
- `frontend/rust-lib/flowy-search/src/entities/notification.rs`
  - `frontend.rust-lib.flowy-search.src.entities.notification.SearchStatePB` (L5-L11) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.notification.SearchNotification` (L14-L18) - Enum
  - `frontend.rust-lib.flowy-search.src.entities.notification.i32.from` (L21-L23) - Function
  - `frontend.rust-lib.flowy-search.src.entities.notification.SearchNotification.from` (L27-L32) - Function
- `frontend/rust-lib/flowy-search/src/entities/query.rs`
  - `frontend.rust-lib.flowy-search.src.entities.query.SearchQueryPB` (L4-L16) - Struct
- `frontend/rust-lib/flowy-search/src/entities/result.rs`
  - `frontend.rust-lib.flowy-search.src.entities.result.SearchResponsePB` (L9-L29) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.RepeatedSearchSummaryPB` (L32-L35) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.SearchSummaryPB` (L38-L47) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.SearchSourcePB` (L50-L59) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.RepeatedSearchResponseItemPB` (L62-L65) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.SearchResponseItemPB` (L68-L83) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.RepeatedLocalSearchResponseItemPB` (L86-L89) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.LocalSearchResponseItemPB` (L92-L104) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.ResultIconTypePB` (L107-L112) - Enum
  - `frontend.rust-lib.flowy-search.src.entities.result.IconType.from` (L115-L121) - Function
  - `frontend.rust-lib.flowy-search.src.entities.result.ResultIconTypePB.from` (L135-L142) - Function
  - `frontend.rust-lib.flowy-search.src.entities.result.i64.from` (L146-L152) - Function
  - `frontend.rust-lib.flowy-search.src.entities.result.ResultIconPB` (L156-L162) - Struct
  - `frontend.rust-lib.flowy-search.src.entities.result.ViewIcon.from` (L165-L170) - Function
  - `frontend.rust-lib.flowy-search.src.entities.result.ResultIconPB.from` (L183-L188) - Function
- `frontend/rust-lib/flowy-search/src/entities/search_filter.rs`
  - `frontend.rust-lib.flowy-search.src.entities.search_filter.SearchFilterPB` (L4-L7) - Struct
- `frontend/rust-lib/flowy-search/src/event_handler.rs`
  - `frontend.rust-lib.flowy-search.src.event_handler.upgrade_manager` (L8-L15) - Function
  - `frontend.rust-lib.flowy-search.src.event_handler.stream_search_handler` (L18-L36) - Function
- `frontend/rust-lib/flowy-search/src/event_map.rs`
  - `frontend.rust-lib.flowy-search.src.event_map.init` (L9-L14) - Function
  - `frontend.rust-lib.flowy-search.src.event_map.SearchEvent` (L18-L21) - Enum
- `frontend/rust-lib/flowy-search/src/services/manager.rs`
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchType` (L19-L23) - Enum
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchHandler` (L26-L36) - Interface
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchHandler.search_type` (L28-L28) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchHandler.perform_search` (L31-L35) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager` (L42-L46) - Struct
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.new` (L49-L60) - Function
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.get_handler` (L62-L64) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.create_local_document_search` (L66-L76) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.on_launch_if_authenticated` (L78-L85) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.initialize_after_sign_in` (L87-L94) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.initialize_after_sign_up` (L96-L103) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.initialize_after_open_workspace` (L105-L112) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.perform_search` (L114-L117) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.perform_search_with_sink` (L119-L211) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.SearchManager.drop` (L215-L217) - Method
  - `frontend.rust-lib.flowy-search.src.services.manager.is_current_search` (L220-L229) - Function


### Index Storage and Abstraction
Provides Tantivy-based full-text document indexing, schema configurations, and cloud search interfaces.


**Related Classes/Methods**:

- `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState`:15-29
- `frontend.rust-lib.flowy-search-pub.src.schema.LocalSearchTantivySchema`
- `frontend.rust-lib.flowy-search-pub.src.cloud.SearchCloudService`:9-22
- `frontend.rust-lib.flowy-search-pub.src.entities.TanvitySearchResponseItem`:34-41



**Source Files:**

- `frontend/rust-lib/flowy-search-pub/src/cloud.rs`
  - `frontend.rust-lib.flowy-search-pub.src.cloud.SearchCloudService` (L9-L22) - Interface
  - `frontend.rust-lib.flowy-search-pub.src.cloud.SearchCloudService.document_search` (L10-L14) - Method
  - `frontend.rust-lib.flowy-search-pub.src.cloud.SearchCloudService.generate_search_summary` (L16-L21) - Method
- `frontend/rust-lib/flowy-search-pub/src/entities.rs`
  - `frontend.rust-lib.flowy-search-pub.src.entities.ViewObserveData` (L8-L14) - Struct
  - `frontend.rust-lib.flowy-search-pub.src.entities.ViewObserveData.from_view` (L17-L25) - Function
  - `frontend.rust-lib.flowy-search-pub.src.entities.FolderViewObserver` (L29-L31) - Interface
  - `frontend.rust-lib.flowy-search-pub.src.entities.FolderViewObserver.set_observer_rx` (L30-L30) - Method
  - `frontend.rust-lib.flowy-search-pub.src.entities.TanvitySearchResponseItem` (L34-L41) - Struct
  - `frontend.rust-lib.flowy-search-pub.src.entities.ResultIcon` (L44-L47) - Struct
- `frontend/rust-lib/flowy-search-pub/src/schema.rs`
  - `frontend.rust-lib.flowy-search-pub.src.schema.LocalSearchTantivySchema` (L3-L3) - Struct
  - `frontend.rust-lib.flowy-search-pub.src.schema.LocalSearchTantivySchema.default` (L6-L8) - Function
  - `frontend.rust-lib.flowy-search-pub.src.schema.LocalSearchTantivySchema.new` (L19-L28) - Function
- `frontend/rust-lib/flowy-search-pub/src/tantivy_state.rs`
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState` (L15-L29) - Struct
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.new` (L32-L87) - Function
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.add_document` (L89-L105) - Method
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.add_document_content` (L107-L194) - Method
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.add_document_metadata` (L196-L290) - Method
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.delete_workspace` (L292-L298) - Method
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.delete_document` (L301-L308) - Method
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.delete_documents` (L310-L319) - Method
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state.DocumentTantivyState.search` (L321-L449) - Method
- `frontend/rust-lib/flowy-search-pub/src/tantivy_state_init.rs`
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state_init.get_or_init_document_tantivy_state` (L16-L34) - Function
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state_init.close_document_tantivy_state` (L36-L43) - Function
  - `frontend.rust-lib.flowy-search-pub.src.tantivy_state_init.get_document_tantivy_state` (L45-L52) - Function




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)