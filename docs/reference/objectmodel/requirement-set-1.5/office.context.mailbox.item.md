---
title: Office.context.mailbox.item - requirement set 1.5
description: 'Outlook Mailbox API requirement set 1.5 version of the Item object model.'
ms.date: 07/16/2021
localization_priority: Normal
---

# item (Mailbox requirement set 1.5)

### [Office](office.md)[.context](office.context.md)[.mailbox](office.context.mailbox.md).item

`item` is used to access the currently selected message, meeting request, or appointment. You can determine the type of the item by using the `itemType` property.

##### Requirements

|Requirement|Value|
|---|---|
|[Minimum mailbox requirement set version](../../requirement-sets/outlook-api-requirement-sets.md)|1.1|
|[Minimum permission level](../../../outlook/understanding-outlook-add-in-permissions.md)|Restricted|
|[Applicable Outlook mode](../../../outlook/outlook-add-ins-overview.md#extension-points)|Appointment Organizer, Appointment Attendee,<br>Message Compose, or Message Read|

> [!IMPORTANT]
> Android and iOS: There are limitations on when add-ins activate and which APIs are available. To learn more, refer to [Add mobile support to an Outlook add-in](../../../outlook/add-mobile-support.md#compose-mode-and-appointments).

## Properties

| Property | Minimum<br>permission level | Details by mode | Return type | Minimum<br>requirement set |
|---|---|---|---|:---:|
| attachments | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#attachments) | Array.<[AttachmentDetails](/javascript/api/outlook/office.attachmentdetails)> | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#attachments) | Array.<[AttachmentDetails](/javascript/api/outlook/office.attachmentdetails)> | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| bcc | ReadItem | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#bcc) | [Recipients](/javascript/api/outlook/office.recipients) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| body | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#body) | [Body](/javascript/api/outlook/office.body) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#body) | [Body](/javascript/api/outlook/office.body) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#body) | [Body](/javascript/api/outlook/office.body) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#body) | [Body](/javascript/api/outlook/office.body) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| cc | ReadItem | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#cc) | [Recipients](/javascript/api/outlook/office.recipients) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#cc) | Array.<[EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails)> | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| conversationId | ReadItem | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#conversationId) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#conversationId) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| dateTimeCreated | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#dateTimeCreated) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#dateTimeCreated) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| dateTimeModified | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#dateTimeModified) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#dateTimeModified) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| end | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#end) | [Time](/javascript/api/outlook/office.time) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#end) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#end)<br>(Meeting Request) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| from | ReadItem | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#from) | [EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| internetMessageId | ReadItem | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#internetMessageId) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| itemClass | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#itemClass) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#itemClass) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| itemId | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#itemId) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#itemId) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| itemType | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#itemType) | [MailboxEnums.ItemType](/javascript/api/outlook/office.mailboxenums.itemtype) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#itemType) | [MailboxEnums.ItemType](/javascript/api/outlook/office.mailboxenums.itemtype) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#itemType) | [MailboxEnums.ItemType](/javascript/api/outlook/office.mailboxenums.itemtype) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#itemType) | [MailboxEnums.ItemType](/javascript/api/outlook/office.mailboxenums.itemtype) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| location | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#location) | [Location](/javascript/api/outlook/office.location) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#location) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#location)<br>(Meeting Request) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| normalizedSubject | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#normalizedSubject) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#normalizedSubject) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| notificationMessages | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#notificationMessages) | [NotificationMessages](/javascript/api/outlook/office.notificationmessages) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#notificationMessages) | [NotificationMessages](/javascript/api/outlook/office.notificationmessages) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#notificationMessages) | [NotificationMessages](/javascript/api/outlook/office.notificationmessages) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#notificationMessages) | [NotificationMessages](/javascript/api/outlook/office.notificationmessages) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| optionalAttendees | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#optionalAttendees) | [Recipients](/javascript/api/outlook/office.recipients) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#optionalAttendees) | Array.<[EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails)> | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| organizer | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#organizer) | [EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| requiredAttendees | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#requiredAttendees) | [Recipients](/javascript/api/outlook/office.recipients) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#requiredAttendees) | Array.<[EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails)> | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| sender | ReadItem | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#sender) | [EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| start | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#start) | [Time](/javascript/api/outlook/office.time) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#start) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#start)<br>(Meeting Request) | Date | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| subject | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#subject) | [Subject](/javascript/api/outlook/office.subject) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#subject) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#subject) | [Subject](/javascript/api/outlook/office.subject) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#subject) | String | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| to | ReadItem | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#to) | [Recipients](/javascript/api/outlook/office.recipients) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#to) | Array.<[EmailAddressDetails](/javascript/api/outlook/office.emailaddressdetails)> | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |

## Methods

| Method | Minimum<br>permission level | Details by mode | Minimum<br>requirement set |
|---|---|---|:---:|
| addFileAttachmentAsync(uri, attachmentName, [options], [callback]) | ReadWriteItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#addFileAttachmentAsync_uri__attachmentName__options__callback_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#addFileAttachmentAsync_uri__attachmentName__options__callback_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| addItemAttachmentAsync(itemId, attachmentName, [options], [callback]) | ReadWriteItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#addItemAttachmentAsync_itemId__attachmentName__options__callback_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#addItemAttachmentAsync_itemId__attachmentName__options__callback_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| close() | Restricted | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#close__) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#close__) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| displayReplyAllForm(formData) | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#displayReplyAllForm_formData_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#displayReplyAllForm_formData_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| displayReplyForm(formData) | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#displayReplyForm_formData_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#displayReplyForm_formData_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| getEntities() | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#getEntities__) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#getEntities__) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| getEntitiesByType(entityType) | Restricted | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#getEntitiesByType_entityType_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#getEntitiesByType_entityType_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| getFilteredEntitiesByName(name) | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#getFilteredEntitiesByName_name_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#getFilteredEntitiesByName_name_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| getRegExMatches() | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#getRegExMatches__) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#getRegExMatches__) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| getRegExMatchesByName(name) | ReadItem | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#getRegExMatchesByName_name_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#getRegExMatchesByName_name_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| getSelectedDataAsync(coercionType, [options], callback) | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#getSelectedDataAsync_coercionType__options__callback_) | [1.2](../requirement-set-1.2/outlook-requirement-set-1.2.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#getSelectedDataAsync_coercionType__options__callback_) | [1.2](../requirement-set-1.2/outlook-requirement-set-1.2.md) |
| loadCustomPropertiesAsync(callback, [userContext]) | ReadItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#loadCustomPropertiesAsync_callback__userContext_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Appointment Attendee](/javascript/api/outlook/office.appointmentread?view=outlook-js-1.5&preserve-view=true#loadCustomPropertiesAsync_callback__userContext_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#loadCustomPropertiesAsync_callback__userContext_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| | | [Message Read](/javascript/api/outlook/office.messageread?view=outlook-js-1.5&preserve-view=true#loadCustomPropertiesAsync_callback__userContext_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| removeAttachmentAsync(attachmentId, [options], [callback]) | ReadWriteItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#removeAttachmentAsync_attachmentId__options__callback_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
|  |  | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#removeAttachmentAsync_attachmentId__options__callback_) | [1.1](../requirement-set-1.1/outlook-requirement-set-1.1.md) |
| saveAsync([options], callback) | ReadWriteItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#saveAsync_options__callback_) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#saveAsync_options__callback_) | [1.3](../requirement-set-1.3/outlook-requirement-set-1.3.md) |
| setSelectedDataAsync(data, [options], callback) | ReadWriteItem | [Appointment Organizer](/javascript/api/outlook/office.appointmentcompose?view=outlook-js-1.5&preserve-view=true#setSelectedDataAsync_data__options__callback_) | [1.2](../requirement-set-1.2/outlook-requirement-set-1.2.md) |
| | | [Message Compose](/javascript/api/outlook/office.messagecompose?view=outlook-js-1.5&preserve-view=true#setSelectedDataAsync_data__options__callback_) | [1.2](../requirement-set-1.2/outlook-requirement-set-1.2.md) |

## Example

The following JavaScript code example shows how to access the `subject` property of the current item in Outlook.

```js
// The initialize function is required for all apps.
Office.initialize = function () {
  // Checks for the DOM to load using the jQuery ready function.
  $(document).ready(function () {
    // After the DOM is loaded, app-specific code can run.
    var item = Office.context.mailbox.item;
    var subject = item.subject;
    // Continue with processing the subject of the current item,
    // which can be a message or appointment.
  });
};
```
