# Update

**Description** : *Object contains info on events occurred*

**Layer** : 211

```tl
updateNewMessage#1f2b0afd message:Message pts:int pts_count:int = Update;
updateMessageID#4e90bfd6 id:int random_id:long = Update;
updateDeleteMessages#a20db0e5 messages:Vector<int> pts:int pts_count:int = Update;
updateUserTyping#c01e857f user_id:long action:SendMessageAction = Update;
updateChatUserTyping#83487af0 chat_id:long from_id:Peer action:SendMessageAction = Update;
updateChatParticipants#7761198 participants:ChatParticipants = Update;
updateUserStatus#e5bdf8de user_id:long status:UserStatus = Update;
updateUserName#a7848924 user_id:long first_name:string last_name:string usernames:Vector<Username> = Update;
updateNewAuthorization#8951abef flags:# unconfirmed:flags.0?true hash:long date:flags.0?int device:flags.0?string location:flags.0?string = Update;
updateNewEncryptedMessage#12bcbd9a message:EncryptedMessage qts:int = Update;
updateEncryptedChatTyping#1710f156 chat_id:int = Update;
updateEncryption#b4a2e88d chat:EncryptedChat date:int = Update;
updateEncryptedMessagesRead#38fe25b7 chat_id:int max_date:int date:int = Update;
updateChatParticipantAdd#3dda5451 chat_id:long user_id:long inviter_id:long date:int version:int = Update;
updateChatParticipantDelete#e32f3d77 chat_id:long user_id:long version:int = Update;
updateDcOptions#8e5e9873 dc_options:Vector<DcOption> = Update;
updateNotifySettings#bec268ef peer:NotifyPeer notify_settings:PeerNotifySettings = Update;
updateServiceNotification#ebe46819 flags:# popup:flags.0?true invert_media:flags.2?true inbox_date:flags.1?int type:string message:string media:MessageMedia entities:Vector<MessageEntity> = Update;
updatePrivacy#ee3b272a key:PrivacyKey rules:Vector<PrivacyRule> = Update;
updateUserPhone#5492a13 user_id:long phone:string = Update;
updateReadHistoryInbox#9c974fdf flags:# folder_id:flags.0?int peer:Peer max_id:int still_unread_count:int pts:int pts_count:int = Update;
updateReadHistoryOutbox#2f2f21bf peer:Peer max_id:int pts:int pts_count:int = Update;
updateWebPage#7f891213 webpage:WebPage pts:int pts_count:int = Update;
updateReadMessagesContents#f8227181 flags:# messages:Vector<int> pts:int pts_count:int date:flags.0?int = Update;
updateChannelTooLong#108d941f flags:# channel_id:long pts:flags.0?int = Update;
updateChannel#635b4c09 channel_id:long = Update;
updateNewChannelMessage#62ba04d9 message:Message pts:int pts_count:int = Update;
updateReadChannelInbox#922e6e10 flags:# folder_id:flags.0?int channel_id:long max_id:int still_unread_count:int pts:int = Update;
updateDeleteChannelMessages#c32d5b12 channel_id:long messages:Vector<int> pts:int pts_count:int = Update;
updateChannelMessageViews#f226ac08 channel_id:long id:int views:int = Update;
updateChatParticipantAdmin#d7ca61a2 chat_id:long user_id:long is_admin:Bool version:int = Update;
updateNewStickerSet#688a30aa stickerset:messages.StickerSet = Update;
updateStickerSetsOrder#bb2d201 flags:# masks:flags.0?true emojis:flags.1?true order:Vector<long> = Update;
updateStickerSets#31c24808 flags:# masks:flags.0?true emojis:flags.1?true = Update;
updateSavedGifs#9375341e = Update;
updateBotInlineQuery#496f379c flags:# query_id:long user_id:long query:string geo:flags.0?GeoPoint peer_type:flags.1?InlineQueryPeerType offset:string = Update;
updateBotInlineSend#12f12a07 flags:# user_id:long query:string geo:flags.0?GeoPoint id:string msg_id:flags.1?InputBotInlineMessageID = Update;
updateEditChannelMessage#1b3f4df7 message:Message pts:int pts_count:int = Update;
updateBotCallbackQuery#b9cfc48d flags:# query_id:long user_id:long peer:Peer msg_id:int chat_instance:long data:flags.0?bytes game_short_name:flags.1?string = Update;
updateEditMessage#e40370a3 message:Message pts:int pts_count:int = Update;
updateInlineBotCallbackQuery#691e9052 flags:# query_id:long user_id:long msg_id:InputBotInlineMessageID chat_instance:long data:flags.0?bytes game_short_name:flags.1?string = Update;
updateReadChannelOutbox#b75f99a9 channel_id:long max_id:int = Update;
updateDraftMessage#edfc111e flags:# peer:Peer top_msg_id:flags.0?int saved_peer_id:flags.1?Peer draft:DraftMessage = Update;
updateReadFeaturedStickers#571d2742 = Update;
updateRecentStickers#9a422c20 = Update;
updateConfig#a229dd06 = Update;
updatePtsChanged#3354678f = Update;
updateChannelWebPage#2f2ba99f channel_id:long webpage:WebPage pts:int pts_count:int = Update;
updateDialogPinned#6e6fe51c flags:# pinned:flags.0?true folder_id:flags.1?int peer:DialogPeer = Update;
updatePinnedDialogs#fa0f3ca2 flags:# folder_id:flags.1?int order:flags.0?Vector<DialogPeer> = Update;
updateBotWebhookJSON#8317c0c3 data:DataJSON = Update;
updateBotWebhookJSONQuery#9b9240a6 query_id:long data:DataJSON timeout:int = Update;
updateBotShippingQuery#b5aefd7d query_id:long user_id:long payload:bytes shipping_address:PostAddress = Update;
updateBotPrecheckoutQuery#8caa9a96 flags:# query_id:long user_id:long payload:bytes info:flags.0?PaymentRequestedInfo shipping_option_id:flags.1?string currency:string total_amount:long = Update;
updatePhoneCall#ab0f6b1e phone_call:PhoneCall = Update;
updateLangPackTooLong#46560264 lang_code:string = Update;
updateLangPack#56022f4d difference:LangPackDifference = Update;
updateFavedStickers#e511996d = Update;
updateChannelReadMessagesContents#25f324f7 flags:# channel_id:long top_msg_id:flags.0?int saved_peer_id:flags.1?Peer messages:Vector<int> = Update;
updateContactsReset#7084a7be = Update;
updateChannelAvailableMessages#b23fc698 channel_id:long available_min_id:int = Update;
updateDialogUnreadMark#b658f23e flags:# unread:flags.0?true peer:DialogPeer saved_peer_id:flags.1?Peer = Update;
updateMessagePoll#aca1657b flags:# poll_id:long poll:flags.0?Poll results:PollResults = Update;
updateChatDefaultBannedRights#54c01850 peer:Peer default_banned_rights:ChatBannedRights version:int = Update;
updateFolderPeers#19360dc0 folder_peers:Vector<FolderPeer> pts:int pts_count:int = Update;
updatePeerSettings#6a7e7366 peer:Peer settings:PeerSettings = Update;
updatePeerLocated#b4afcfb0 peers:Vector<PeerLocated> = Update;
updateNewScheduledMessage#39a51dfb message:Message = Update;
updateDeleteScheduledMessages#f2a71983 flags:# peer:Peer messages:Vector<int> sent_messages:flags.0?Vector<int> = Update;
updateTheme#8216fba3 theme:Theme = Update;
updateGeoLiveViewed#871fb939 peer:Peer msg_id:int = Update;
updateLoginToken#564fe691 = Update;
updateMessagePollVote#24f40e77 poll_id:long peer:Peer options:Vector<bytes> qts:int = Update;
updateDialogFilter#26ffde7d flags:# id:int filter:flags.0?DialogFilter = Update;
updateDialogFilterOrder#a5d72105 order:Vector<int> = Update;
updateDialogFilters#3504914f = Update;
updatePhoneCallSignalingData#2661bf09 phone_call_id:long data:bytes = Update;
updateChannelMessageForwards#d29a27f4 channel_id:long id:int forwards:int = Update;
updateReadChannelDiscussionInbox#d6b19546 flags:# channel_id:long top_msg_id:int read_max_id:int broadcast_id:flags.0?long broadcast_post:flags.0?int = Update;
updateReadChannelDiscussionOutbox#695c9e7c channel_id:long top_msg_id:int read_max_id:int = Update;
updatePeerBlocked#ebe07752 flags:# blocked:flags.0?true blocked_my_stories_from:flags.1?true peer_id:Peer = Update;
updateChannelUserTyping#8c88c923 flags:# channel_id:long top_msg_id:flags.0?int from_id:Peer action:SendMessageAction = Update;
updatePinnedMessages#ed85eab5 flags:# pinned:flags.0?true peer:Peer messages:Vector<int> pts:int pts_count:int = Update;
updatePinnedChannelMessages#5bb98608 flags:# pinned:flags.0?true channel_id:long messages:Vector<int> pts:int pts_count:int = Update;
updateChat#f89a6a4e chat_id:long = Update;
updateGroupCallParticipants#f2ebdb4e call:InputGroupCall participants:Vector<GroupCallParticipant> version:int = Update;
updateGroupCall#97d64341 flags:# chat_id:flags.0?long call:GroupCall = Update;
updatePeerHistoryTTL#bb9bb9a5 flags:# peer:Peer ttl_period:flags.0?int = Update;
updateChatParticipant#d087663a flags:# chat_id:long date:int actor_id:long user_id:long prev_participant:flags.0?ChatParticipant new_participant:flags.1?ChatParticipant invite:flags.2?ExportedChatInvite qts:int = Update;
updateChannelParticipant#985d3abb flags:# via_chatlist:flags.3?true channel_id:long date:int actor_id:long user_id:long prev_participant:flags.0?ChannelParticipant new_participant:flags.1?ChannelParticipant invite:flags.2?ExportedChatInvite qts:int = Update;
updateBotStopped#c4870a49 user_id:long date:int stopped:Bool qts:int = Update;
updateGroupCallConnection#b783982 flags:# presentation:flags.0?true params:DataJSON = Update;
updateBotCommands#4d712f2e peer:Peer bot_id:long commands:Vector<BotCommand> = Update;
updatePendingJoinRequests#7063c3db peer:Peer requests_pending:int recent_requesters:Vector<long> = Update;
updateBotChatInviteRequester#11dfa986 peer:Peer date:int user_id:long about:string invite:ExportedChatInvite qts:int = Update;
updateMessageReactions#1e297bfa flags:# peer:Peer msg_id:int top_msg_id:flags.0?int saved_peer_id:flags.1?Peer reactions:MessageReactions = Update;
updateAttachMenuBots#17b7a20b = Update;
updateWebViewResultSent#1592b79d query_id:long = Update;
updateBotMenuButton#14b85813 bot_id:long button:BotMenuButton = Update;
updateSavedRingtones#74d8be99 = Update;
updateTranscribedAudio#84cd5a flags:# pending:flags.0?true peer:Peer msg_id:int transcription_id:long text:string = Update;
updateReadFeaturedEmojiStickers#fb4c496c = Update;
updateUserEmojiStatus#28373599 user_id:long emoji_status:EmojiStatus = Update;
updateRecentEmojiStatuses#30f443db = Update;
updateRecentReactions#6f7863f4 = Update;
updateMoveStickerSetToTop#86fccf85 flags:# masks:flags.0?true emojis:flags.1?true stickerset:long = Update;
updateMessageExtendedMedia#d5a41724 peer:Peer msg_id:int extended_media:Vector<MessageExtendedMedia> = Update;
updateChannelPinnedTopic#192efbe3 flags:# pinned:flags.0?true channel_id:long topic_id:int = Update;
updateChannelPinnedTopics#fe198602 flags:# channel_id:long order:flags.0?Vector<int> = Update;
updateUser#20529438 user_id:long = Update;
updateAutoSaveSettings#ec05b097 = Update;
updateStory#75b3b798 peer:Peer story:StoryItem = Update;
updateReadStories#f74e932b peer:Peer max_id:int = Update;
updateStoryID#1bf335b9 id:int random_id:long = Update;
updateStoriesStealthMode#2c084dc1 stealth_mode:StoriesStealthMode = Update;
updateSentStoryReaction#7d627683 peer:Peer story_id:int reaction:Reaction = Update;
updateBotChatBoost#904dd49c peer:Peer boost:Boost qts:int = Update;
updateChannelViewForumAsMessages#7b68920 channel_id:long enabled:Bool = Update;
updatePeerWallpaper#ae3f101d flags:# wallpaper_overridden:flags.1?true peer:Peer wallpaper:flags.0?WallPaper = Update;
updateBotMessageReaction#ac21d3ce peer:Peer msg_id:int date:int actor:Peer old_reactions:Vector<Reaction> new_reactions:Vector<Reaction> qts:int = Update;
updateBotMessageReactions#9cb7759 peer:Peer msg_id:int date:int reactions:Vector<ReactionCount> qts:int = Update;
updateSavedDialogPinned#aeaf9e74 flags:# pinned:flags.0?true peer:DialogPeer = Update;
updatePinnedSavedDialogs#686c85a6 flags:# order:flags.0?Vector<DialogPeer> = Update;
updateSavedReactionTags#39c67432 = Update;
updateSmsJob#f16269d4 job_id:string = Update;
updateQuickReplies#f9470ab2 quick_replies:Vector<QuickReply> = Update;
updateNewQuickReply#f53da717 quick_reply:QuickReply = Update;
updateDeleteQuickReply#53e6f1ec shortcut_id:int = Update;
updateQuickReplyMessage#3e050d0f message:Message = Update;
updateDeleteQuickReplyMessages#566fe7cd shortcut_id:int messages:Vector<int> = Update;
updateBotBusinessConnect#8ae5c97a connection:BotBusinessConnection qts:int = Update;
updateBotNewBusinessMessage#9ddb347c flags:# connection_id:string message:Message reply_to_message:flags.0?Message qts:int = Update;
updateBotEditBusinessMessage#7df587c flags:# connection_id:string message:Message reply_to_message:flags.0?Message qts:int = Update;
updateBotDeleteBusinessMessage#a02a982e connection_id:string peer:Peer messages:Vector<int> qts:int = Update;
updateNewStoryReaction#1824e40b story_id:int peer:Peer reaction:Reaction = Update;
updateStarsBalance#4e80a379 balance:StarsAmount = Update;
updateBusinessBotCallbackQuery#1ea2fda7 flags:# query_id:long user_id:long connection_id:string message:Message reply_to_message:flags.2?Message chat_instance:long data:flags.0?bytes = Update;
updateStarsRevenueStatus#a584b019 peer:Peer status:StarsRevenueStatus = Update;
updateBotPurchasedPaidMedia#283bd312 user_id:long payload:string qts:int = Update;
updatePaidReactionPrivacy#8b725fce private:PaidReactionPrivacy = Update;
updateSentPhoneCode#504aa18f sent_code:auth.SentCode = Update;
updateGroupCallChainBlocks#a477288f call:InputGroupCall sub_chain_id:int blocks:Vector<bytes> next_offset:int = Update;
updateReadMonoForumInbox#77b0e372 channel_id:long saved_peer_id:Peer read_max_id:int = Update;
updateReadMonoForumOutbox#a4a79376 channel_id:long saved_peer_id:Peer read_max_id:int = Update;
updateMonoForumNoPaidException#9f812b08 flags:# exception:flags.0?true channel_id:long saved_peer_id:Peer = Update;
```

---

## Constructors

| Constructor | Description |
| :---: | :--- |
| [**updateNewMessage**](constructor/updateNewMessage) | New message in a private chat or in a basic group |
| [**updateMessageID**](constructor/updateMessageID) | Sent message with random_id client identifier was assigned an identifier |
| [**updateDeleteMessages**](constructor/updateDeleteMessages) | Messages were deleted |
| [**updateUserTyping**](constructor/updateUserTyping) | The user is preparing a message; typing, recording, uploading, etc. This update is valid for 6 seconds. If no further updates of this kind are received after 6 seconds, it should be considered that the user stopped doing whatever they were doing |
| [**updateChatUserTyping**](constructor/updateChatUserTyping) | The user is preparing a message in a group; typing, recording, uploading, etc. This update is valid for 6 seconds. If no further updates of this kind are received after 6 seconds, it should be considered that the user stopped doing whatever they were doing |
| [**updateChatParticipants**](constructor/updateChatParticipants) | Composition of chat participants changed |
| [**updateUserStatus**](constructor/updateUserStatus) | Contact status update |
| [**updateUserName**](constructor/updateUserName) | Changes the user's first name, last name and username |
| [**updateNewAuthorization**](constructor/updateNewAuthorization) | A new session logged into the current user's account through an unknown device |
| [**updateNewEncryptedMessage**](constructor/updateNewEncryptedMessage) | New encrypted message |
| [**updateEncryptedChatTyping**](constructor/updateEncryptedChatTyping) | Interlocutor is typing a message in an encrypted chat. Update period is 6 second. If upon this time there is no repeated update, it shall be considered that the interlocutor stopped typing |
| [**updateEncryption**](constructor/updateEncryption) | Change of state in an encrypted chat |
| [**updateEncryptedMessagesRead**](constructor/updateEncryptedMessagesRead) | Communication history in an encrypted chat was marked as read |
| [**updateChatParticipantAdd**](constructor/updateChatParticipantAdd) | New group member |
| [**updateChatParticipantDelete**](constructor/updateChatParticipantDelete) | A member has left the group |
| [**updateDcOptions**](constructor/updateDcOptions) | Changes in the data center configuration options |
| [**updateNotifySettings**](constructor/updateNotifySettings) | Changes in notification settings |
| [**updateServiceNotification**](constructor/updateServiceNotification) | A service message for the user.The app must show the message to the user upon receiving this update. In case the popup parameter was passed, the text message must be displayed in a popup alert immediately upon receipt. It is recommended to handle the text as you would an ordinary message in terms of highlighting links, etc. The message must also be stored locally as part of the message history with the user id 777000 (Telegram Notifications) |
| [**updatePrivacy**](constructor/updatePrivacy) | Privacy rules were changed |
| [**updateUserPhone**](constructor/updateUserPhone) | A user's phone number was changed |
| [**updateReadHistoryInbox**](constructor/updateReadHistoryInbox) | Incoming messages were read |
| [**updateReadHistoryOutbox**](constructor/updateReadHistoryOutbox) | Outgoing messages were read |
| [**updateWebPage**](constructor/updateWebPage) | An instant view webpage preview was generated |
| [**updateReadMessagesContents**](constructor/updateReadMessagesContents) | Contents of messages in the common message box were read |
| [**updateChannelTooLong**](constructor/updateChannelTooLong) | There are new updates in the specified channel, the client must fetch them.  If the difference is too long or if the channel isn't currently in the states, start fetching from the specified pts |
| [**updateChannel**](constructor/updateChannel) | Channel/supergroup (channel and/or channelFull) information was updated.This update can only be received through getDifference or in updates/updatesCombined constructors, so it will always come bundled with the updated channel, that should be applied as usual », without re-fetching the info manually.However, full peer information will not come bundled in updates, so the full peer cache (channelFull) must be invalidated for channel_id when receiving this update |
| [**updateNewChannelMessage**](constructor/updateNewChannelMessage) | A new message was sent in a channel/supergroup |
| [**updateReadChannelInbox**](constructor/updateReadChannelInbox) | Incoming messages in a channel/supergroup were read |
| [**updateDeleteChannelMessages**](constructor/updateDeleteChannelMessages) | Some messages in a supergroup/channel were deleted |
| [**updateChannelMessageViews**](constructor/updateChannelMessageViews) | The view counter of a message in a channel has changed |
| [**updateChatParticipantAdmin**](constructor/updateChatParticipantAdmin) | Admin permissions of a user in a basic group were changed |
| [**updateNewStickerSet**](constructor/updateNewStickerSet) | A new stickerset was installed |
| [**updateStickerSetsOrder**](constructor/updateStickerSetsOrder) | The order of stickersets was changed |
| [**updateStickerSets**](constructor/updateStickerSets) | Installed stickersets have changed, the client should refetch them as described in the docs |
| [**updateSavedGifs**](constructor/updateSavedGifs) | The saved gif list has changed, the client should refetch it using messages.getSavedGifs |
| [**updateBotInlineQuery**](constructor/updateBotInlineQuery) | An incoming inline query |
| [**updateBotInlineSend**](constructor/updateBotInlineSend) | The result of an inline query that was chosen by a user and sent to their chat partner. Please see our documentation on the feedback collecting for details on how to enable these updates for your bot |
| [**updateEditChannelMessage**](constructor/updateEditChannelMessage) | A message was edited in a channel/supergroup |
| [**updateBotCallbackQuery**](constructor/updateBotCallbackQuery) | A callback button was pressed, and the button data was sent to the bot that created the button |
| [**updateEditMessage**](constructor/updateEditMessage) | A message was edited |
| [**updateInlineBotCallbackQuery**](constructor/updateInlineBotCallbackQuery) | This notification is received by bots when a button is pressed |
| [**updateReadChannelOutbox**](constructor/updateReadChannelOutbox) | Outgoing messages in a channel/supergroup were read |
| [**updateDraftMessage**](constructor/updateDraftMessage) | Notifies a change of a message draft |
| [**updateReadFeaturedStickers**](constructor/updateReadFeaturedStickers) | Some featured stickers were marked as read |
| [**updateRecentStickers**](constructor/updateRecentStickers) | The recent sticker list was updated |
| [**updateConfig**](constructor/updateConfig) | The server-side configuration has changed; the client should re-fetch the config using help.getConfig and help.getAppConfig |
| [**updatePtsChanged**](constructor/updatePtsChanged) | Common message box sequence PTS has changed, state has to be refetched using updates.getState |
| [**updateChannelWebPage**](constructor/updateChannelWebPage) | A webpage preview of a link in a channel/supergroup message was generated |
| [**updateDialogPinned**](constructor/updateDialogPinned) | A dialog was pinned/unpinned |
| [**updatePinnedDialogs**](constructor/updatePinnedDialogs) | Pinned dialogs were updated |
| [**updateBotWebhookJSON**](constructor/updateBotWebhookJSON) | A new incoming event; for bots only |
| [**updateBotWebhookJSONQuery**](constructor/updateBotWebhookJSONQuery) | A new incoming query; for bots only |
| [**updateBotShippingQuery**](constructor/updateBotShippingQuery) | This object contains information about an incoming shipping query |
| [**updateBotPrecheckoutQuery**](constructor/updateBotPrecheckoutQuery) | This object contains information about an incoming pre-checkout query |
| [**updatePhoneCall**](constructor/updatePhoneCall) | An incoming phone call |
| [**updateLangPackTooLong**](constructor/updateLangPackTooLong) | A language pack has changed, the client should manually fetch the changed strings using langpack.getDifference |
| [**updateLangPack**](constructor/updateLangPack) | Language pack updated |
| [**updateFavedStickers**](constructor/updateFavedStickers) | The list of favorited stickers was changed, the client should call messages.getFavedStickers to refetch the new list |
| [**updateChannelReadMessagesContents**](constructor/updateChannelReadMessagesContents) | The specified channel/supergroup messages were read |
| [**updateContactsReset**](constructor/updateContactsReset) | All contacts were deleted |
| [**updateChannelAvailableMessages**](constructor/updateChannelAvailableMessages) | The history of a channel/supergroup was hidden |
| [**updateDialogUnreadMark**](constructor/updateDialogUnreadMark) | The manual unread mark of a chat was changed |
| [**updateMessagePoll**](constructor/updateMessagePoll) | The results of a poll have changed |
| [**updateChatDefaultBannedRights**](constructor/updateChatDefaultBannedRights) | Default banned rights in a normal chat were updated |
| [**updateFolderPeers**](constructor/updateFolderPeers) | The peer list of a peer folder was updated |
| [**updatePeerSettings**](constructor/updatePeerSettings) | Settings of a certain peer have changed |
| [**updatePeerLocated**](constructor/updatePeerLocated) | List of peers near you was updated |
| [**updateNewScheduledMessage**](constructor/updateNewScheduledMessage) | A message was added to the schedule queue of a chat |
| [**updateDeleteScheduledMessages**](constructor/updateDeleteScheduledMessages) | Some scheduled messages were deleted (or sent) from the schedule queue of a chat |
| [**updateTheme**](constructor/updateTheme) | A cloud theme was updated |
| [**updateGeoLiveViewed**](constructor/updateGeoLiveViewed) | Live geoposition message was viewed |
| [**updateLoginToken**](constructor/updateLoginToken) | A login token (for login via QR code) was accepted |
| [**updateMessagePollVote**](constructor/updateMessagePollVote) | A specific peer has voted in a poll |
| [**updateDialogFilter**](constructor/updateDialogFilter) | A new folder was added |
| [**updateDialogFilterOrder**](constructor/updateDialogFilterOrder) | New folder order |
| [**updateDialogFilters**](constructor/updateDialogFilters) | Clients should update folder info |
| [**updatePhoneCallSignalingData**](constructor/updatePhoneCallSignalingData) | Incoming phone call signaling payload |
| [**updateChannelMessageForwards**](constructor/updateChannelMessageForwards) | The forward counter of a message in a channel has changed |
| [**updateReadChannelDiscussionInbox**](constructor/updateReadChannelDiscussionInbox) | Incoming comments in a discussion thread were marked as read |
| [**updateReadChannelDiscussionOutbox**](constructor/updateReadChannelDiscussionOutbox) | Outgoing comments in a discussion thread were marked as read |
| [**updatePeerBlocked**](constructor/updatePeerBlocked) | We blocked a peer, see here » for more info on blocklists |
| [**updateChannelUserTyping**](constructor/updateChannelUserTyping) | A user is typing in a supergroup, channel or message thread |
| [**updatePinnedMessages**](constructor/updatePinnedMessages) | Some messages were pinned in a chat |
| [**updatePinnedChannelMessages**](constructor/updatePinnedChannelMessages) | Messages were pinned/unpinned in a channel/supergroup |
| [**updateChat**](constructor/updateChat) | Chat (chat and/or chatFull) information was updated.This update can only be received through getDifference or in updates/updatesCombined constructors, so it will always come bundled with the updated chat, that should be applied as usual », without re-fetching the info manually.However, full peer information will not come bundled in updates, so the full peer cache (chatFull) must be invalidated for chat_id when receiving this update |
| [**updateGroupCallParticipants**](constructor/updateGroupCallParticipants) | The participant list of a certain group call has changed |
| [**updateGroupCall**](constructor/updateGroupCall) | A new groupcall was started |
| [**updatePeerHistoryTTL**](constructor/updatePeerHistoryTTL) | The Time-To-Live for messages sent by the current user in a specific chat has changed |
| [**updateChatParticipant**](constructor/updateChatParticipant) | A user has joined or left a specific chat |
| [**updateChannelParticipant**](constructor/updateChannelParticipant) | A participant has left, joined, was banned or admined in a channel or supergroup |
| [**updateBotStopped**](constructor/updateBotStopped) | A bot was stopped or re-started |
| [**updateGroupCallConnection**](constructor/updateGroupCallConnection) | New WebRTC parameters |
| [**updateBotCommands**](constructor/updateBotCommands) | The command set of a certain bot in a certain chat has changed |
| [**updatePendingJoinRequests**](constructor/updatePendingJoinRequests) | Someone has requested to join a chat or channel |
| [**updateBotChatInviteRequester**](constructor/updateBotChatInviteRequester) | Someone has requested to join a chat or channel (bots only, users will receive an updatePendingJoinRequests, instead) |
| [**updateMessageReactions**](constructor/updateMessageReactions) | New message reactions » are available |
| [**updateAttachMenuBots**](constructor/updateAttachMenuBots) | The list of installed attachment menu entries » has changed, use messages.getAttachMenuBots to fetch the updated list |
| [**updateWebViewResultSent**](constructor/updateWebViewResultSent) | Indicates to a bot that a webview was closed and an inline message was sent on behalf of the user using messages.sendWebViewResultMessage |
| [**updateBotMenuButton**](constructor/updateBotMenuButton) | The menu button behavior for the specified bot has changed |
| [**updateSavedRingtones**](constructor/updateSavedRingtones) | The list of saved notification sounds has changed, use account.getSavedRingtones to fetch the new list |
| [**updateTranscribedAudio**](constructor/updateTranscribedAudio) | A pending voice message transcription » initiated with messages.transcribeAudio was updated |
| [**updateReadFeaturedEmojiStickers**](constructor/updateReadFeaturedEmojiStickers) | Some featured custom emoji stickers were marked as read |
| [**updateUserEmojiStatus**](constructor/updateUserEmojiStatus) | The emoji status of a certain user has changed |
| [**updateRecentEmojiStatuses**](constructor/updateRecentEmojiStatuses) | The list of recent emoji statuses has changed |
| [**updateRecentReactions**](constructor/updateRecentReactions) | The list of recent message reactions has changed |
| [**updateMoveStickerSetToTop**](constructor/updateMoveStickerSetToTop) | A stickerset was just moved to top, see here for more info » |
| [**updateMessageExtendedMedia**](constructor/updateMessageExtendedMedia) | You bought a paid media »: this update contains the revealed media |
| [**updateChannelPinnedTopic**](constructor/updateChannelPinnedTopic) | A forum topic » was pinned or unpinned |
| [**updateChannelPinnedTopics**](constructor/updateChannelPinnedTopics) | The pinned topics of a forum have changed |
| [**updateUser**](constructor/updateUser) | User (user and/or userFull) information was updated.This update can only be received through getDifference or in updates/updatesCombined constructors, so it will always come bundled with the updated user, that should be applied as usual », without re-fetching the info manually.However, full peer information will not come bundled in updates, so the full peer cache (userFull) must be invalidated for user_id when receiving this update |
| [**updateAutoSaveSettings**](constructor/updateAutoSaveSettings) | Media autosave settings have changed and must be refetched using account.getAutoSaveSettings |
| [**updateStory**](constructor/updateStory) | A new story was posted |
| [**updateReadStories**](constructor/updateReadStories) | Stories of a specific peer were marked as read |
| [**updateStoryID**](constructor/updateStoryID) | A story was successfully uploaded.Once a story is successfully uploaded, an updateStoryID will be returned, indicating the story ID (id) that was attributed to the story (like for messages, random_id indicates the random_id that was passed to stories.sendStory: this way, you can tell which story was assigned a specific id by checking which stories.sendStory call has the returned random_id) |
| [**updateStoriesStealthMode**](constructor/updateStoriesStealthMode) | Indicates that stories stealth mode was activated |
| [**updateSentStoryReaction**](constructor/updateSentStoryReaction) | Indicates we reacted to a story » |
| [**updateBotChatBoost**](constructor/updateBotChatBoost) | A channel/supergroup boost has changed (bots only) |
| [**updateChannelViewForumAsMessages**](constructor/updateChannelViewForumAsMessages) | Users may also choose to display messages from all topics as if they were sent to a normal group, using a "View as messages" setting in the local client.  This setting only affects the current account, and is synced to other logged in sessions using the channels.toggleViewForumAsMessages method; invoking this method will update the value of the view_forum_as_messages flag of channelFull or dialog and emit an updateChannelViewForumAsMessages |
| [**updatePeerWallpaper**](constructor/updatePeerWallpaper) | The wallpaper » of a given peer has changed |
| [**updateBotMessageReaction**](constructor/updateBotMessageReaction) | Bots only: a user has changed their reactions on a message with public reactions |
| [**updateBotMessageReactions**](constructor/updateBotMessageReactions) | Bots only: the number of reactions on a message with anonymous reactions has changed |
| [**updateSavedDialogPinned**](constructor/updateSavedDialogPinned) | A saved message dialog was pinned/unpinned |
| [**updatePinnedSavedDialogs**](constructor/updatePinnedSavedDialogs) | Pinned saved dialogs » were updated |
| [**updateSavedReactionTags**](constructor/updateSavedReactionTags) | The list of reaction tag » names assigned by the user has changed and should be refetched using messages.getSavedReactionTags » |
| [**updateSmsJob**](constructor/updateSmsJob) | A new SMS job was received |
| [**updateQuickReplies**](constructor/updateQuickReplies) | Info about or the order of quick reply shortcuts » was changed |
| [**updateNewQuickReply**](constructor/updateNewQuickReply) | A new quick reply shortcut » was created |
| [**updateDeleteQuickReply**](constructor/updateDeleteQuickReply) | A quick reply shortcut » was deleted. This will not emit updateDeleteQuickReplyMessages updates, even if all the messages in the shortcut are also deleted by this update |
| [**updateQuickReplyMessage**](constructor/updateQuickReplyMessage) | A new message was added to a quick reply shortcut » |
| [**updateDeleteQuickReplyMessages**](constructor/updateDeleteQuickReplyMessages) | One or more messages in a quick reply shortcut » were deleted |
| [**updateBotBusinessConnect**](constructor/updateBotBusinessConnect) | Connecting or disconnecting a business bot or changing the connection settings will emit an updateBotBusinessConnect update to the bot, with the new settings and a connection_id that will be used by the bot to handle updates from and send messages as the user |
| [**updateBotNewBusinessMessage**](constructor/updateBotNewBusinessMessage) | A message was received via a connected business chat » |
| [**updateBotEditBusinessMessage**](constructor/updateBotEditBusinessMessage) | A message was edited in a connected business chat » |
| [**updateBotDeleteBusinessMessage**](constructor/updateBotDeleteBusinessMessage) | A message was deleted in a connected business chat » |
| [**updateNewStoryReaction**](constructor/updateNewStoryReaction) | Represents a new reaction to a story |
| [**updateStarsBalance**](constructor/updateStarsBalance) | The current account's Telegram Stars balance » has changed |
| [**updateBusinessBotCallbackQuery**](constructor/updateBusinessBotCallbackQuery) | A callback button sent via a business connection was pressed, and the button data was sent to the bot that created the button |
| [**updateStarsRevenueStatus**](constructor/updateStarsRevenueStatus) | The Telegram Star balance of a channel/bot we own has changed » |
| [**updateBotPurchasedPaidMedia**](constructor/updateBotPurchasedPaidMedia) | Bots only: a user has purchased a paid media |
| [**updatePaidReactionPrivacy**](constructor/updatePaidReactionPrivacy) | Contains the current default paid reaction privacy, see here » for more info.Clients should invoke messages.getPaidReactionPrivacy on startup to fetch the current default reaction privacy because this update is only sent to currently online sessions and cannot be fetched using getDifference on client startup |
| [**updateSentPhoneCode**](constructor/updateSentPhoneCode) | NOTHING |
| [**updateGroupCallChainBlocks**](constructor/updateGroupCallChainBlocks) | NOTHING |
| [**updateReadMonoForumInbox**](constructor/updateReadMonoForumInbox) | NOTHING |
| [**updateReadMonoForumOutbox**](constructor/updateReadMonoForumOutbox) | NOTHING |
| [**updateMonoForumNoPaidException**](constructor/updateMonoForumNoPaidException) | NOTHING |