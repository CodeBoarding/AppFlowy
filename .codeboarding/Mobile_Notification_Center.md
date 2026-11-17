```mermaid
graph LR
    Notification_Tab_Views["Notification Tab Views"]
    Notification_Screen_Pages["Notification Screen Pages"]
    Shared_Notification_Elements["Shared Notification Elements"]
    Notification_Tab_Views -- "renders shared visual elements" --> Shared_Notification_Elements
    Notification_Screen_Pages -- "embeds notification tab views" --> Notification_Tab_Views
```

[![CodeBoarding](https://img.shields.io/badge/Generated%20by-CodeBoarding-9cf?style=flat-square)](https://github.com/CodeBoarding/CodeBoarding)[![Web platform](https://img.shields.io/badge/Open%20in-Web%20platform-2563EB?style=flat-square)](https://app.codeboarding.org)[![Demo](https://img.shields.io/badge/Try%20our-Demo-blue?style=flat-square)](https://www.codeboarding.org/diagrams)[![Contact](https://img.shields.io/badge/Contact%20us%20-%20contact@codeboarding.org-lightgrey?style=flat-square)](mailto:contact@codeboarding.org)

## Details

Displays user reminders and notifications with multi-selection management and contextual item actions.

### Notification Tab Views
Provides notification tabs, list views, and individual notification card widgets with swipe actions and empty states.


**Related Classes/Methods**:

- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.NotificationTab`:15-25
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.MultiSelectNotificationTab`:104-137
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item.NotificationItem`:15-94
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item.MultiSelectNotificationItem`:11-86



**Source Files:**

- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/empty.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.empty.EmptyNotification` (L8-L58) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.empty.EmptyNotification.EmptyNotification` (L9-L12) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.empty.EmptyNotification.build` (L17-L57) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/multi_select_notification_item.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item.MultiSelectNotificationItem` (L11-L86) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item.MultiSelectNotificationItem.MultiSelectNotificationItem` (L12-L15) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item.MultiSelectNotificationItem.build` (L20-L85) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item._InnerNotificationItem` (L88-L113) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item._InnerNotificationItem._InnerNotificationItem` (L89-L91) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.multi_select_notification_item._InnerNotificationItem.build` (L96-L112) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/notification_item.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item.NotificationItem` (L15-L94) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item.NotificationItem.NotificationItem` (L16-L20) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item.NotificationItem.build` (L26-L93) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item._InnerNotificationItem` (L96-L118) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item._InnerNotificationItem._InnerNotificationItem` (L97-L100) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item._InnerNotificationItem.build` (L106-L117) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item._SlidableNotificationItem` (L120-L171) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item._SlidableNotificationItem._SlidableNotificationItem` (L121-L125) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.notification_item._SlidableNotificationItem.build` (L132-L170) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/slide_actions.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions.NotificationPaneActionType` (L16-L83) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions.NotificationPaneActionType.more` (L17-L17) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions.NotificationPaneActionType.markAsRead` (L18-L18) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions.NotificationPaneActionType.unArchive` (L20-L20) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions.NotificationPaneActionType.actionButton` (L22-L82) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions.NotificationPaneActionExtension.onMoreAction` (L86-L113) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions._NotificationMoreActions` (L116-L210) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions._NotificationMoreActions._NotificationMoreActions` (L117-L119) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions._NotificationMoreActions.build` (L124-L165) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions._NotificationMoreActions._onMarkAsRead` (L167-L183) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions._NotificationMoreActions._onMultipleChoice` (L185-L189) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.slide_actions._NotificationMoreActions._onArchive` (L191-L209) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/tab.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.NotificationTab` (L15-L25) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.NotificationTab.NotificationTab` (L16-L19) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.NotificationTab.createState` (L24-L24) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab._NotificationTabState` (L27-L102) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab._NotificationTabState.wantKeepAlive` (L30-L30) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab._NotificationTabState.build` (L33-L66) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab._NotificationTabState._onRefresh` (L68-L81) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab._NotificationTabState._filterReminders` (L83-L101) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.MultiSelectNotificationTab` (L104-L137) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.MultiSelectNotificationTab.MultiSelectNotificationTab` (L105-L107) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab.MultiSelectNotificationTab.build` (L110-L136) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/tab_bar.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab_bar.MobileNotificationTabBar` (L6-L55) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab_bar.MobileNotificationTabBar.MobileNotificationTabBar` (L7-L12) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.tab_bar.MobileNotificationTabBar.build` (L19-L54) - Method


### Notification Screen Pages
Hosts the mobile notification screens, navigation headers, multi-select mode pages, and settings menus.


**Related Classes/Methods**:

- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsScreenV2`:17-25
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsTab`:70-75
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationsMultiSelectScreen`:9-21
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page.MobileNotificationsScreen`:19-27



**Source Files:**

- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/mobile_notifications_multiple_select_page.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationsMultiSelectScreen` (L9-L21) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationsMultiSelectScreen.MobileNotificationsMultiSelectScreen` (L10-L10) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationsMultiSelectScreen.build` (L15-L20) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationMultiSelect` (L23-L31) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationMultiSelect.MobileNotificationMultiSelect` (L24-L26) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page.MobileNotificationMultiSelect.createState` (L29-L30) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page._MobileNotificationMultiSelectState` (L33-L59) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page._MobileNotificationMultiSelectState.dispose` (L36-L40) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_multiple_select_page._MobileNotificationMultiSelectState.build` (L43-L58) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/mobile_notifications_page.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page.MobileNotificationsScreen` (L19-L27) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page.MobileNotificationsScreen.MobileNotificationsScreen` (L20-L20) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page.MobileNotificationsScreen.createState` (L25-L26) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._MobileNotificationsScreenState` (L29-L65) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._MobileNotificationsScreenState.build` (L35-L64) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._NotificationScreenContent` (L67-L165) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._NotificationScreenContent._NotificationScreenContent` (L68-L73) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._NotificationScreenContent.build` (L81-L151) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._NotificationScreenContent._onAction` (L153-L160) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_page._NotificationScreenContent._onReadChanged` (L162-L164) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/mobile_notifications_screen.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsScreenV2` (L17-L25) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsScreenV2.MobileNotificationsScreenV2` (L18-L18) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsScreenV2.createState` (L23-L24) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsScreenV2State` (L27-L68) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsScreenV2State.wantKeepAlive` (L31-L31) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsScreenV2State.initState` (L34-L38) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsScreenV2State.dispose` (L41-L45) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsScreenV2State.build` (L48-L65) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsScreenV2State._onRefresh` (L67-L67) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsTab` (L70-L75) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsTab.MobileNotificationsTab` (L71-L71) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen.MobileNotificationsTab.createState` (L74-L74) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsTabState` (L77-L123) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsTabState.initState` (L88-L91) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsTabState.dispose` (L94-L97) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.mobile_notifications_screen._MobileNotificationsTabState.build` (L100-L122) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/header.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationPageHeader` (L9-L34) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationPageHeader.MobileNotificationPageHeader` (L10-L12) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationPageHeader.build` (L15-L33) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationMultiSelectPageHeader` (L36-L96) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationMultiSelectPageHeader.MobileNotificationMultiSelectPageHeader` (L37-L39) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationMultiSelectPageHeader.build` (L42-L74) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.header.MobileNotificationMultiSelectPageHeader._buildCancelButton` (L77-L95) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/mobile_notification_tab_bar.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar.MobileNotificationTabBar` (L7-L15) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar.MobileNotificationTabBar.MobileNotificationTabBar` (L8-L8) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar.MobileNotificationTabBar.createState` (L13-L14) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar._MobileNotificationTabBarState` (L17-L75) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar._MobileNotificationTabBarState.initState` (L19-L22) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar._MobileNotificationTabBarState.dispose` (L25-L28) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar._MobileNotificationTabBarState._updateState` (L30-L30) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.mobile_notification_tab_bar._MobileNotificationTabBarState.build` (L33-L74) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/settings_popup_menu.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._NotificationSettingsPopupMenuItem` (L15-L21) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._NotificationSettingsPopupMenuItem.settings` (L16-L16) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._NotificationSettingsPopupMenuItem.markAllAsRead` (L17-L17) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._NotificationSettingsPopupMenuItem.archiveAll` (L18-L18) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._NotificationSettingsPopupMenuItem.unarchiveAll` (L20-L20) - Enum
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu` (L23-L139) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu.NotificationSettingsPopupMenu` (L24-L24) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu.build` (L27-L92) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu._buildItem` (L94-L107) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu._onMarkAllAsRead` (L109-L117) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu._onArchiveAll` (L119-L126) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu.NotificationSettingsPopupMenu._onUnarchiveAll` (L128-L138) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._PopupButton` (L141-L167) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._PopupButton._PopupButton` (L142-L145) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.settings_popup_menu._PopupButton.build` (L151-L166) - Method


### Shared Notification Elements
Supplies shared visual elements, status indicators, badges, content preview renderers, and color helpers for notifications.


**Related Classes/Methods**:

- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationContent`:115-125
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationIcon`:24-69
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationCheckIcon`:71-90
- `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.UnreadRedDot`:92-113



**Source Files:**

- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/color.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.color.NotificationItemColors.notificationItemTextColor` (L5-L10) - Method
- `frontend/appflowy_flutter/lib/mobile/presentation/notifications/widgets/shared.dart`
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationIcon` (L24-L69) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationIcon.NotificationIcon` (L25-L29) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationIcon.build` (L35-L68) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationCheckIcon` (L71-L90) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationCheckIcon.NotificationCheckIcon` (L72-L72) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationCheckIcon.build` (L77-L89) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.UnreadRedDot` (L92-L113) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.UnreadRedDot.UnreadRedDot` (L93-L93) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.UnreadRedDot.build` (L96-L112) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationContent` (L115-L125) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationContent.NotificationContent` (L116-L119) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationContent.createState` (L124-L124) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState` (L127-L262) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState.theme` (L128-L128) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState.didUpdateWidget` (L131-L137) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState.build` (L140-L162) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState._buildContent` (L164-L191) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState._buildHeader` (L193-L219) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared._NotificationContentState._buildPageName` (L221-L261) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationEllipse` (L264-L279) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationEllipse.NotificationEllipse` (L265-L265) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationEllipse.build` (L268-L278) - Method
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationDocumentContent` (L281-L366) - Class
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationDocumentContent.NotificationDocumentContent` (L282-L286) - Constructor
  - `frontend.appflowy_flutter.lib.mobile.presentation.notifications.widgets.shared.NotificationDocumentContent.build` (L292-L365) - Method




### [FAQ](https://github.com/CodeBoarding/GeneratedOnBoardings/tree/main?tab=readme-ov-file#faq)