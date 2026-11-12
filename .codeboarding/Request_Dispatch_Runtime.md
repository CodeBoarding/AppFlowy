```mermaid
graph LR
    Event_Dispatcher_Orchestration["Event Dispatcher Orchestration"]
    Response_Modeling_and_Errors["Response Modeling and Errors"]
    Plugin_Registry_and_State["Plugin Registry and State"]
    Request_Payload_Extraction["Request Payload Extraction"]
    Service_Pipeline_and_Handlers["Service Pipeline and Handlers"]
    Event_Dispatcher_Orchestration -- "returns dispatch responses" --> Response_Modeling_and_Errors
    Event_Dispatcher_Orchestration -- "routes events to plugins" --> Plugin_Registry_and_State
    Plugin_Registry_and_State -- "builds handler services" --> Service_Pipeline_and_Handlers
    Request_Payload_Extraction -- "constructs typed responses" --> Response_Modeling_and_Errors
    Service_Pipeline_and_Handlers -- "encapsulates request state" --> Request_Payload_Extraction
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Provides asynchronous request routing, module registration, payload decoding, and response dispatching.

### Event Dispatcher Orchestration
Orchestrates asynchronous and synchronous event dispatching to registered plugins across the runtime.


**Related Classes/Methods**:

- `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher`:63-67
- `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchService`:237-239
- `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchContext`:224-228
- `frontend.rust-lib.lib-dispatch.src.runtime.AFPluginRuntime`:9-11



**Source Files:**

- `frontend/rust-lib/lib-dispatch/src/byte_trait.rs`
  - `frontend.rust-lib.lib-dispatch.src.byte_trait.ToBytes` (L6-L8) - Interface
  - `frontend.rust-lib.lib-dispatch.src.byte_trait.ToBytes.into_bytes` (L7-L7) - Method
  - `frontend.rust-lib.lib-dispatch.src.byte_trait.T.into_bytes` (L15-L27) - Method
  - `frontend.rust-lib.lib-dispatch.src.byte_trait.AFPluginFromBytes` (L30-L32) - Interface
  - `frontend.rust-lib.lib-dispatch.src.byte_trait.AFPluginFromBytes.parse_from_bytes` (L31-L31) - Function
  - `frontend.rust-lib.lib-dispatch.src.byte_trait.T.parse_from_bytes` (L42-L54) - Function
- `frontend/rust-lib/lib-dispatch/src/dispatcher.rs`
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFConcurrent` (L26-L26) - Interface
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.downcast_owned` (L45-L47) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher` (L63-L67) - Struct
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher.new` (L70-L76) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher.async_send` (L79-L84) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.async_send_with_callback` (L86-L96) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.boxed_async_send_with_callback` (L99-L131) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher.async_send_with_callback` (L134-L167) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher.boxed_async_send_with_callback` (L170-L207) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.AFPluginDispatcher.sync_send` (L210-L219) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchContext` (L224-L228) - Struct
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchContext.into_parts` (L231-L234) - Method
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchService` (L237-L239) - Struct
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchService.call` (L247-L290) - Method
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.plugin_info` (L294-L300) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.print_plugins` (L303-L307) - Function
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchFuture` (L310-L313) - Struct
  - `frontend.rust-lib.lib-dispatch.src.dispatcher.DispatchFuture.poll` (L321-L324) - Method
- `frontend/rust-lib/lib-dispatch/src/macros.rs`
  - `frontend.rust-lib.lib-dispatch.src.macros.dispatch_future` (L2-L8) - Function
- `frontend/rust-lib/lib-dispatch/src/runtime.rs`
  - `frontend.rust-lib.lib-dispatch.src.runtime.AFPluginRuntime` (L9-L11) - Struct
  - `frontend.rust-lib.lib-dispatch.src.runtime.AFPluginRuntime.fmt` (L14-L20) - Method
  - `frontend.rust-lib.lib-dispatch.src.runtime.AFPluginRuntime.new` (L24-L27) - Function
  - `frontend.rust-lib.lib-dispatch.src.runtime.AFPluginRuntime.spawn` (L30-L36) - Method
  - `frontend.rust-lib.lib-dispatch.src.runtime.AFPluginRuntime.block_on` (L39-L44) - Method
  - `frontend.rust-lib.lib-dispatch.src.runtime.default_tokio_runtime` (L57-L77) - Function
- `frontend/rust-lib/lib-dispatch/src/util/ready.rs`
  - `frontend.rust-lib.lib-dispatch.src.util.ready.Ready` (L7-L9) - Struct
  - `frontend.rust-lib.lib-dispatch.src.util.ready.Ready.into_inner` (L13-L15) - Method
  - `frontend.rust-lib.lib-dispatch.src.util.ready.Ready.poll` (L24-L27) - Method
  - `frontend.rust-lib.lib-dispatch.src.util.ready.ready` (L30-L32) - Function


### Response Modeling and Errors
Defines event response envelopes, response builders, responders, and dispatch error classifications.


**Related Classes/Methods**:

- `frontend.rust-lib.lib-dispatch.src.response.response.AFPluginEventResponse`:22-26
- `frontend.rust-lib.lib-dispatch.src.response.builder.ResponseBuilder`:15-18
- `frontend.rust-lib.lib-dispatch.src.response.responder.AFPluginResponder`:9-11
- `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError`:29-31



**Source Files:**

- `frontend/rust-lib/lib-dispatch/src/errors/errors.rs`
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.Error` (L14-L16) - Interface
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.Error.as_response` (L15-L15) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.from` (L21-L25) - Function
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError` (L29-L31) - Struct
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.inner_error` (L34-L36) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.fmt` (L40-L42) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.fmt` (L46-L48) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.source` (L52-L54) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.cause` (L56-L58) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.from` (L75-L77) - Function
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.parse_from_bytes` (L81-L84) - Function
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.AFPluginEventResponse.from` (L88-L90) - Function
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.DispatchError.serialize` (L94-L102) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.InternalError` (L106-L114) - Enum
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.InternalError.fmt` (L117-L127) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.InternalError.as_response` (L131-L133) - Method
  - `frontend.rust-lib.lib-dispatch.src.errors.errors.InternalError.from` (L137-L139) - Function
- `frontend/rust-lib/lib-dispatch/src/response/builder.rs`
  - `frontend.rust-lib.lib-dispatch.src.response.builder.static_response` (L6-L13) - Function
  - `frontend.rust-lib.lib-dispatch.src.response.builder.ResponseBuilder` (L15-L18) - Struct
  - `frontend.rust-lib.lib-dispatch.src.response.builder.ResponseBuilder.new` (L21-L26) - Function
  - `frontend.rust-lib.lib-dispatch.src.response.builder.ResponseBuilder.data` (L28-L31) - Method
  - `frontend.rust-lib.lib-dispatch.src.response.builder.ResponseBuilder.build` (L33-L38) - Method
- `frontend/rust-lib/lib-dispatch/src/response/responder.rs`
  - `frontend.rust-lib.lib-dispatch.src.response.responder.AFPluginResponder` (L9-L11) - Interface
  - `frontend.rust-lib.lib-dispatch.src.response.responder.AFPluginResponder.respond_to` (L10-L10) - Method
  - `frontend.rust-lib.lib-dispatch.src.response.responder.impl_responder` (L13-L21) - Function
  - `frontend.rust-lib.lib-dispatch.src.response.responder.Result.respond_to` (L35-L40) - Method
- `frontend/rust-lib/lib-dispatch/src/response/response.rs`
  - `frontend.rust-lib.lib-dispatch.src.response.response.StatusCode` (L14-L17) - Enum
  - `frontend.rust-lib.lib-dispatch.src.response.response.AFPluginEventResponse` (L22-L26) - Struct
  - `frontend.rust-lib.lib-dispatch.src.response.response.AFPluginEventResponse.new` (L29-L34) - Function
  - `frontend.rust-lib.lib-dispatch.src.response.response.AFPluginEventResponse.parse` (L36-L51) - Method
  - `frontend.rust-lib.lib-dispatch.src.response.response.AFPluginEventResponse.fmt` (L55-L64) - Method
  - `frontend.rust-lib.lib-dispatch.src.response.response.AFPluginEventResponse.respond_to` (L69-L71) - Method
  - `frontend.rust-lib.lib-dispatch.src.response.response.data_result_ok` (L76-L81) - Function


### Plugin Registry and State
Manages plugin definitions, event route maps, and shared state storage for registered extensions.


**Related Classes/Methods**:

- `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin`:64-76
- `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginEvent`
- `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginService`:191-196



**Source Files:**

- `frontend/rust-lib/lib-dispatch/src/module/container.rs`
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap` (L6-L6) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.new` (L10-L12) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.insert` (L14-L22) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.remove` (L24-L29) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.get` (L31-L39) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.get_mut` (L41-L49) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.contains` (L51-L56) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.container.AFPluginStateMap.extend` (L58-L60) - Method
- `frontend/rust-lib/lib-dispatch/src/module/data.rs`
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState` (L10-L10) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState.new` (L16-L18) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState.get_ref` (L20-L22) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState.deref` (L31-L33) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState.clone` (L40-L42) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState.from` (L49-L51) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.data.AFPluginState.from_request` (L62-L73) - Function
- `frontend/rust-lib/lib-dispatch/src/module/module.rs`
  - `frontend.rust-lib.lib-dispatch.src.module.module.plugin_map_or_crash` (L28-L47) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginEvent` (L50-L50) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginEvent.from` (L53-L55) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin` (L64-L76) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.default` (L79-L86) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.new` (L90-L92) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.name` (L94-L97) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.state` (L99-L104) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.event` (L107-L125) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.events` (L127-L133) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginRequest` (L141-L145) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginRequest.new` (L148-L157) - Function
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginRequest.payload` (L159-L165) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginRequest.fmt` (L169-L171) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPlugin.new_service` (L181-L188) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginService` (L191-L196) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginService.call` (L204-L229) - Method
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginServiceFuture` (L233-L236) - Struct
  - `frontend.rust-lib.lib-dispatch.src.module.module.AFPluginServiceFuture.poll` (L241-L244) - Method


### Request Payload Extraction
Models incoming requests, payload buffers, and provides type-safe extraction from event requests.


**Related Classes/Methods**:

- `frontend.rust-lib.lib-dispatch.src.request.request.AFPluginEventRequest`:20-26
- `frontend.rust-lib.lib-dispatch.src.request.request.FromAFPluginRequest`:52-57
- `frontend.rust-lib.lib-dispatch.src.request.payload.Payload`:7-10
- `frontend.rust-lib.lib-dispatch.src.data.AFPluginData`



**Source Files:**

- `frontend/rust-lib/lib-dispatch/src/data.rs`
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginDataValidator` (L15-L19) - Interface
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginDataValidator.validate` (L16-L18) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData` (L21-L21) - Struct
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.into_inner` (L24-L26) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.try_into_inner` (L33-L36) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.deref` (L42-L44) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.validate` (L51-L54) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.deref_mut` (L58-L60) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.from_request` (L71-L81) - Function
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.respond_to` (L88-L99) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.try_from` (L107-L109) - Function
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.try_from` (L117-L119) - Function
  - `frontend.rust-lib.lib-dispatch.src.data.parse_payload` (L122-L139) - Function
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.try_into` (L147-L151) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.into_bytes` (L155-L157) - Method
  - `frontend.rust-lib.lib-dispatch.src.data.AFPluginData.fmt` (L164-L166) - Method
- `frontend/rust-lib/lib-dispatch/src/request/payload.rs`
  - `frontend.rust-lib.lib-dispatch.src.request.payload.Payload` (L7-L10) - Enum
  - `frontend.rust-lib.lib-dispatch.src.request.payload.Payload.to_vec` (L13-L18) - Method
  - `frontend.rust-lib.lib-dispatch.src.request.payload.Payload.as_ref` (L22-L27) - Method
  - `frontend.rust-lib.lib-dispatch.src.request.payload.fmt` (L31-L33) - Method
  - `frontend.rust-lib.lib-dispatch.src.request.payload.Payload.fmt` (L37-L39) - Method
  - `frontend.rust-lib.lib-dispatch.src.request.payload.format_payload_print` (L42-L47) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.payload.from` (L50-L52) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.payload.Payload.from` (L79-L81) - Function
- `frontend/rust-lib/lib-dispatch/src/request/request.rs`
  - `frontend.rust-lib.lib-dispatch.src.request.request.AFPluginEventRequest` (L20-L26) - Struct
  - `frontend.rust-lib.lib-dispatch.src.request.request.AFPluginEventRequest.new` (L29-L38) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.request.AFPluginEventRequest.get_state` (L40-L49) - Method
  - `frontend.rust-lib.lib-dispatch.src.request.request.FromAFPluginRequest` (L52-L57) - Interface
  - `frontend.rust-lib.lib-dispatch.src.request.request.FromAFPluginRequest.from_request` (L56-L56) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.request.().from_request` (L64-L66) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.request.String.from_request` (L74-L79) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.request.unexpected_none_payload` (L82-L85) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.request.Result.from_request` (L95-L99) - Function
  - `frontend.rust-lib.lib-dispatch.src.request.request.FromRequestFuture` (L103-L106) - Struct
  - `frontend.rust-lib.lib-dispatch.src.request.request.FromRequestFuture.poll` (L114-L118) - Method


### Service Pipeline and Handlers
Provides service interfaces, factory wrappers, and handler traits for invoking plugin logic.


**Related Classes/Methods**:

- `frontend.rust-lib.lib-dispatch.src.service.service.Service`:8-14
- `frontend.rust-lib.lib-dispatch.src.service.service.AFPluginServiceFactory`:18-26
- `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandler`:21-27
- `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandlerService`:29-38
- `frontend.rust-lib.lib-dispatch.src.service.service.ServiceRequest`:28-31



**Source Files:**

- `frontend/rust-lib/lib-dispatch/src/service/boxed.rs`
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.factory` (L4-L17) - Function
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.BoxServiceFactory` (L43-L43) - Struct
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.BoxServiceFactory.new_service` (L56-L58) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.Box.call` (L91-L93) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.ServiceWrapper` (L96-L98) - Struct
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.ServiceWrapper.new` (L101-L103) - Function
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.ServiceWrapper.call` (L115-L117) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.FactoryWrapper` (L120-L120) - Struct
  - `frontend.rust-lib.lib-dispatch.src.service.boxed.FactoryWrapper.new_service` (L139-L145) - Method
- `frontend/rust-lib/lib-dispatch/src/service/handler.rs`
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandler` (L21-L27) - Interface
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandler.call` (L26-L26) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandlerService` (L29-L38) - Struct
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandlerService.new` (L47-L52) - Function
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandlerService.clone` (L62-L67) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandlerService.new_service` (L83-L85) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.handler.AFPluginHandlerService.call` (L99-L103) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.handler.HandlerServiceFuture` (L107-L116) - Enum
  - `frontend.rust-lib.lib-dispatch.src.service.handler.HandlerServiceFuture.poll` (L127-L153) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.handler.factory_tuple` (L156-L167) - Function
  - `frontend.rust-lib.lib-dispatch.src.service.handler.tuple_from_req` (L169-L228) - Function
- `frontend/rust-lib/lib-dispatch/src/service/service.rs`
  - `frontend.rust-lib.lib-dispatch.src.service.service.Service` (L8-L14) - Interface
  - `frontend.rust-lib.lib-dispatch.src.service.service.Service.call` (L13-L13) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.service.AFPluginServiceFactory` (L18-L26) - Interface
  - `frontend.rust-lib.lib-dispatch.src.service.service.AFPluginServiceFactory.new_service` (L25-L25) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.service.ServiceRequest` (L28-L31) - Struct
  - `frontend.rust-lib.lib-dispatch.src.service.service.ServiceRequest.new` (L34-L39) - Function
  - `frontend.rust-lib.lib-dispatch.src.service.service.ServiceRequest.into_parts` (L42-L44) - Method
  - `frontend.rust-lib.lib-dispatch.src.service.service.ServiceResponse` (L47-L50) - Struct
  - `frontend.rust-lib.lib-dispatch.src.service.service.ServiceResponse.new` (L53-L55) - Function
  - `frontend.rust-lib.lib-dispatch.src.service.service.ServiceResponse.into_parts` (L57-L59) - Method




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)