```mermaid
graph LR
    Backend_FFI_Dispatcher["Backend FFI Dispatcher"]
    Functional_Result_Types["Functional Result Types"]
    Backend_FFI_Dispatcher -- "wraps responses in" --> Functional_Result_Types
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Handles Dart FFI communication and event dispatching to the Rust core engine alongside functional result handling.

### Backend FFI Dispatcher
Dispatches asynchronous requests and manages event streams over foreign function interface bindings to the Rust engine.


**Related Classes/Methods**:

- `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.Dispatch`:50-73
- `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch._extractPayload`:75-101
- `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver`:11-57



**Source Files:**

- `frontend/appflowy_flutter/packages/appflowy_backend/example/lib/main.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main.main` (L8-L10) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main.MyApp` (L12-L15) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main.MyApp.createState` (L14-L14) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main._MyAppState` (L17-L52) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main._MyAppState.initState` (L21-L24) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main._MyAppState.initPlatformState` (L27-L41) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.example.lib.main._MyAppState.build` (L44-L51) - Method
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/appflowy_backend.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.ExceptionType` (L17-L19) - Enum
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.ExceptionType.AppearanceSettingsIsEmpty` (L18-L18) - Enum
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDKException` (L21-L24) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDKException.FlowySDKException` (L23-L23) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDK` (L26-L57) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDK.platformVersion` (L28-L31) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDK.FlowySDK` (L33-L33) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDK.dispose` (L35-L35) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.FlowySDK.init` (L37-L56) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.RustLogStreamReceiver` (L59-L86) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.RustLogStreamReceiver.port` (L64-L64) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.RustLogStreamReceiver.RustLogStreamReceiver._internal` (L66-L75) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.RustLogStreamReceiver.RustLogStreamReceiver` (L77-L79) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend.RustLogStreamReceiver.dispose` (L81-L85) - Method
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/appflowy_backend_method_channel.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_method_channel.MethodChannelFlowySdk` (L7-L18) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_method_channel.MethodChannelFlowySdk.getPlatformVersion` (L13-L17) - Method
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/appflowy_backend_platform_interface.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_platform_interface.AppFlowyBackendPlatform` (L5-L29) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_platform_interface.AppFlowyBackendPlatform.AppFlowyBackendPlatform` (L7-L7) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_platform_interface.AppFlowyBackendPlatform.instance` (L16-L16) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_platform_interface.AppFlowyBackendPlatform.instance=` (L21-L24) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.appflowy_backend_platform_interface.AppFlowyBackendPlatform.getPlatformVersion` (L26-L28) - Method
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/dispatch/dispatch.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.FFIException` (L41-L43) - Enum
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.FFIException.RequestIsEmpty` (L42-L42) - Enum
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.DispatchException` (L45-L48) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.DispatchException.DispatchException` (L47-L47) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.Dispatch` (L50-L73) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.Dispatch.asyncRequest` (L53-L72) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.Dispatch.asyncRequest._asyncRequest` (L56-L61) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch._extractPayload` (L75-L101) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch._extractResponse` (L103-L115) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch._sendToRust` (L117-L134) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.requestToBytes` (L136-L148) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.dispatch.emptyBytes` (L150-L152) - Function
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/dispatch/error.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyInternalError` (L7-L34) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyInternalError.statusCode` (L11-L13) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyInternalError.error` (L15-L17) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyInternalError.has_error` (L19-L21) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyInternalError.toString` (L23-L25) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyInternalError.FlowyInternalError` (L27-L33) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.StackTraceError` (L36-L52) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.StackTraceError.StackTraceError` (L39-L42) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.StackTraceError.asFlowyError` (L44-L47) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.StackTraceError.toString` (L49-L51) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.ErrorListener` (L54-L54) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier` (L58-L112) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.GlobalErrorCodeNotifier._internal` (L66-L66) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.GlobalErrorCodeNotifier` (L69-L71) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.receiveError` (L73-L78) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.receiveErrorBytes` (L80-L90) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.add` (L92-L107) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.add.listener` (L96-L103) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.GlobalErrorCodeNotifier.remove` (L109-L111) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyErrorExtension.isAIResponseLimitExceeded` (L115-L116) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.dispatch.error.FlowyErrorExtension.isStorageLimitExceeded` (L118-L118) - Method
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/ffi.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._open` (L15-L36) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.async_event` (L39-L45) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._invoke_async_C` (L49-L53) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._invoke_async_Dart` (L54-L58) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.sync_event` (L61-L66) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._invoke_sync_C` (L70-L73) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._invoke_sync_Dart` (L74-L77) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.init_sdk` (L80-L85) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._init_sdk_C` (L89-L92) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._init_sdk_Dart` (L93-L96) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.set_stream_port` (L99-L101) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._set_stream_port_C` (L107-L109) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._set_stream_port_Dart` (L110-L112) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.set_log_stream_port` (L115-L117) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._set_log_stream_port_C` (L123-L125) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._set_log_stream_port_Dart` (L126-L128) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.link_me_please` (L131-L133) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._link_me_please_C` (L137-L137) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._link_me_please_Dart` (L138-L138) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.store_dart_post_cobject` (L141-L145) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._store_dart_post_cobject_C` (L150-L152) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._store_dart_post_cobject_Dart` (L153-L155) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.rust_log` (L157-L162) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._invoke_rust_log_C` (L166-L169) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._invoke_rust_log_Dart` (L170-L173) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi.set_env` (L176-L180) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._set_env_C` (L184-L186) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.ffi._set_env_Dart` (L187-L189) - Class
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/log.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log` (L10-L83) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log.Log` (L20-L24) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log._log` (L27-L42) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log.info` (L44-L50) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log.debug` (L52-L58) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log.warn` (L60-L66) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log.trace` (L68-L74) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.Log.error` (L76-L82) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.isReleaseVersion` (L85-L87) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.toNativeUtf8` (L90-L92) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log._formatMessageWithStackTrace` (L94-L99) - Function
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.LogLevelTalkerFilter` (L101-L107) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.log.LogLevelTalkerFilter.filter` (L103-L106) - Method
- `frontend/appflowy_flutter/packages/appflowy_backend/lib/rust_stream.dart`
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.ObserverCallback` (L9-L9) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver` (L11-L57) - Class
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver.port` (L18-L18) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver.observable` (L19-L19) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver.RustStreamReceiver._internal` (L21-L28) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver.RustStreamReceiver` (L30-L32) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver.listen` (L34-L37) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver._streamCallback` (L39-L49) - Method
  - `frontend.appflowy_flutter.packages.appflowy_backend.lib.rust_stream.RustStreamReceiver.dispose` (L51-L56) - Method


### Functional Result Types
Provides functional result encapsulation types for handling asynchronous and synchronous operation outcomes.


**Related Classes/Methods**:

- `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult`:1-25
- `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess`:27-96
- `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure`:98-167



**Source Files:**

- `frontend/appflowy_flutter/packages/appflowy_result/lib/src/async_result.dart`
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.getOrElse` (L7-L9) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.toNullable` (L11-L13) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.getOrThrow` (L15-L17) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.fold` (L19-L24) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.isError` (L26-L28) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.isSuccess` (L30-L32) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.async_result.FlowyAsyncResultExtension.onFailure` (L34-L36) - Method
- `frontend/appflowy_flutter/packages/appflowy_result/lib/src/result.dart`
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult` (L1-L25) - Class
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.FlowyResult` (L2-L2) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.FlowyResult.success` (L4-L4) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.FlowyResult.failure` (L6-L6) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.fold` (L8-L8) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.map` (L10-L10) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.mapError` (L11-L11) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.isSuccess` (L13-L13) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.isFailure` (L14-L14) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.toNullable` (L16-L16) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.onSuccess` (L18-L18) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.onFailure` (L19-L19) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.getOrElse` (L21-L21) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.getOrThrow` (L22-L22) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyResult.getFailure` (L24-L24) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess` (L27-L96) - Class
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.FlowySuccess` (L30-L30) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.value` (L32-L32) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.==` (L35-L39) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.hashCode` (L42-L42) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.toString` (L45-L45) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.fold` (L48-L49) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.map` (L52-L54) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.mapError` (L57-L59) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.isSuccess` (L62-L62) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.isFailure` (L65-L65) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.toNullable` (L68-L70) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.onSuccess` (L73-L75) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.onFailure` (L78-L80) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.getOrElse` (L83-L85) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.getOrThrow` (L88-L90) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowySuccess.getFailure` (L93-L95) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure` (L98-L167) - Class
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.FlowyFailure` (L101-L101) - Constructor
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.error` (L103-L103) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.==` (L106-L110) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.hashCode` (L113-L113) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.toString` (L116-L116) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.fold` (L119-L120) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.map` (L123-L125) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.mapError` (L128-L130) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.isSuccess` (L133-L133) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.isFailure` (L136-L136) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.toNullable` (L139-L141) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.onSuccess` (L144-L146) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.onFailure` (L149-L151) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.getOrElse` (L154-L156) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.getOrThrow` (L159-L161) - Method
  - `frontend.appflowy_flutter.packages.appflowy_result.lib.src.result.FlowyFailure.getFailure` (L164-L166) - Method




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)