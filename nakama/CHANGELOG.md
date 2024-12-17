## 1.2.0

* symlink readme from nakama by @lugehorsam in [#98](https://github.com/heroiclabs/nakama-dart/pull/98)
* Fix account mapping for time related fields by @ilmalte in [#100](https://github.com/heroiclabs/nakama-dart/pull/100)
* Create session restore by @garlen-javier in [#101](https://github.com/heroiclabs/nakama-dart/pull/101)
* Refactored rest client by @fsufyan in [#103](https://github.com/heroiclabs/nakama-dart/pull/103)
* Add missing match presence and remove duplicate session restore by @fsufyan in [#106](https://github.com/heroiclabs/nakama-dart/pull/106)
* Add missing envelope to api.Rpc mapping in WebsocketClient by @rephlex187 in [#116](https://github.com/heroiclabs/nakama-dart/pull/116)
* Include session in request for `NakamaGrpcClient.sessionLogout` by @blaugold in [#110](https://github.com/heroiclabs/nakama-dart/pull/110)
* Fix defaults for `state` parameter of `listFriends`, `listGroupUsers` and `listUserGroups` in `NakamaGrpcClient` by @blaugold in [#109](https://github.com/heroiclabs/nakama-dart/pull/109)
* WASM compatibility by @imaNNeo in [#118](https://github.com/heroiclabs/nakama-dart/pull/118)
* Various improvements example project by @ilmalte in [#119](https://github.com/heroiclabs/nakama-dart/pull/119)

## 1.1.0
- Satori: Adds the Satori SDK for Dart. Satori is our liveops server for game studios. Read more about it in the [documentation](https://heroiclabs.com/docs/satori/concepts/introduction/).

* Fixed: LeaderboardRecordList parsing issue [#52](https://github.com/heroiclabs/nakama-dart/issues/52)
* Added: Module now exports channel_messages [#85](https://github.com/heroiclabs/nakama-dart/pull/85)

## 1.0.5

* Fixed: Cursors are nullable `FriendsList.cursor`, `GroupList.cursor`, `UserGroupList.cursor`, `GroupUserList.cursor`, `NotificationList.cursor`

## 1.0.4

* Fixed: Missing content and subject notification [#80](https://github.com/heroiclabs/nakama-dart/issues/80)

## 1.0.3

* Added missing `http` dependency

## 1.0.2

* Fixed: JWT Expiry was parsed incorrectly so that the session was always expired [#73](https://github.com/heroiclabs/nakama-dart/issues/73)
* Fixed: Auth token was not passed in gRPC calls [#78](https://github.com/heroiclabs/nakama-dart/pull/78)

## 1.0.1

* Added support for signing in with username + password in `authenticateEmail` method

## 1.0.0

* chore: v1.0.0 release 🚀

## 1.0.0-dev.7

* Fixed missing session in rpc call

## 1.0.0-dev.6

* Added creating a match by match name
* Added missing `vars` to session model
* Added `presences` to match

## 1.0.0-dev.5

* **Breaking:** Renamed `ChannelJoinType` enum to `ChannelType`
* **Breaking:** Renamed `leaderboardId` parameter to `leaderboardName` in `writeLeaderboardRecord` and `deleteLeaderboardRecord`
* **Breaking:** `onNotifications` is now a `Stream<Notification>` instead of `Stream<List<Notification>>`
* Added `onPartyData` stream to realtime client
* Added `listTournamentRecordsAroundOwner` to client

## 1.0.0-dev.3

* **Breaking:** Changed signature of `updateGroup` method to match standard update signature. Instead of passing modified model you now have to pass the changed parameters directly to `updateGroup`
* Added rpc request to API client

## 1.0.0-dev.2

* Full removed exported references of the underlaying raw datastructures
* Refactored realtime client

## 1.0.0-dev.1

* Changed License from MIT to Apache 2.0
* **Breaking:** Refactored the SDK to use own models instead of returning the underlaying Protobuf objects
* Most of the functionality added to achieve a stable release:
  * Authentication (Session refresh, missing drivers, linking and unlinking)
  * Leaderboard
  * Friends & Groups
  * Notifications
  * Tournaments
  * Matches

## 0.1.6

* Full storage object support 🎉
* **Breaking** `readStorageObject()` returns now `Future<StorageObject?>` instead of `Future<StorageObject>`. Future resolves with `null` in case there was no element found with given key.
* Adds submitting and listing leaderboard records (more WIP)
* Adds `updateAccount()` method
* Bumps dependencies and API client to latest versions

## 0.1.5

* Adds [Real-Time chat](https://heroiclabs.com/docs/nakama/concepts/chat)
* Fixed missing session passing on `writeStorageObject()` (issue with multiple clients)

## 0.1.4
* Adds `onError()` and `onDone()` callbacks to `NakamaWebsocketClient`

## 0.1.3
* Fixes that the given server key was ignored

## 0.1.2
* Fully implements all authentication methods
* Enhanced documentation and adds link to package

## 0.1.1
* Fixed analyzer issues on web platform
* **Breaking Change:** use `getNakamaClient()` instead of `NakamaBaseClient.adaptive()`

## 0.1.0
* First release